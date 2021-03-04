# How to Clone and Rebuild Conda Env


You have created a conda environment. Good job! But you want it to be accessible to others. And, you want to recreate on a different machine. Well, here is how you can do it.

<!--more-->

Help to **improve this post** on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/how-to-clone-and-recreate-conda-env.md). Thank you for your contribution.

## So you have created a conda environment

To start this off, we will assume that you have created a conda environment and installed some packages on it. If you are not there yet, check out this read: https://machinemind.io/how-to-virtual-env-with-conda/.

To get an overview of the environments that you are operating on your system, type this in your terminal:

```
conda info --envs
```

And, if you want to explore a single environment, you can command the following lines from conda. For example, I have created an environment named "machinemind". Here is how you activate and explore its packages.

```
conda activate machinemind
conda list
```

As we move on to clone and recreate environments, I encorage you to get back to the above commands and use them to track changes.

## Clone a conda environment

Alright, you Dr. Frankenstein, let's clone an environment that we have created on our machine first.

The following command would create a new environment that I have named "machineclone" from the environment "machinemind". It's that simple.

```
conda create --name machineclone --clone machinemind
```

While that may come handy in some cases, we can also think of many cases where you want to export your current environment settings to a file so that you can make your configurations accessible to others.

For that purpose, we will write the environment to a file that we will name "environment.yml". With that file, we can later on recreate our very environment on a different machine. Here is how:

```
cd projects/machinemind
conda activate machinemind
conda env export --no-builds > environment.yml
```

Note that we first navigated to the folder where we wanted the file to be loaded to. In my case, I have navigated to my projects/machinemind directory. And, we activated the environment before cloning.

The --no-builds command unties the environment from the Python version and OS. As you often want to move across different OS, that may be needed (read: https://stackoverflow.com/questions/41274007/anaconda-export-environment-file).

Alternatively, you can create a txt file that can work for the installation process just as well. We will get to it.

```
cd projects/machinemind
conda activate machinemind
conda list --explicit > environment.txt
```

As a good practice, keep the conda of both the systems that you are using, host and remote systen at same speed(read: https://github.com/ContinuumIO/anaconda-issues/issues/9480). A simple update command can help.

```
conda update --all
```

## Recreate a conda environment

Fantastic! The environment was exported in a yml or txt file. "How to handle that thing now?", you might wonder. 

Should you have a yml file, use the following command to recreate the environment. Note that I am again assuming that we first need to navigate to the approproate project directory.

```
cd projects/machinemind
conda env create -f environment.yml
```

You may run into some conflicts when the conda environment is resolved. Don't give up at this stage. Find refuge in updating your conda and manually amending the yml file based on OS dependencies.

In case you obtained a txt file, you may use the following command.

```
cd projects/machinemind
conda create -n machinemind --file environment.txt
conda install -n machinemind --file environment.txt
```

The first line navigates, the second line creates the environment, and the third installs all packages.

## Remove and restore an environment

That was a lot. As we learn to get going with conda environments, a couple of things can go wrong. Expect that to happen. It's fine. Really. Because should you've messed things up, you can always remove the environment. And recreate it from the stored files. Here is the "remove" command.

```
conda remove -n machinemind --all
```

Secondly, conda saves revisions of your environment. You can look them up like this.

```
conda activate machinemind
conda list --revisions
```

And if there is one revision that you'd wish to restore, run the following line.

```
conda install --revision=REVNUM
```

## References

Please visit the conda docs page for getting the latest guide: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html. It's a really good documentation.
