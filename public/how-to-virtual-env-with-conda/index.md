# How to create a virtual environment with conda


Let's say you're working on different projects. One a nlp project. One a financial analytics projects. One a marketing analytics project.
<!--more-->

And let's say, for your first project, you have installed a package some months ago. That package came with verison 1.0. And for another current project you wanted to use an upgraded version of that package - say version 2.0. The package is open source and many changes have been deployed between version 1.0 and 2.0. The code of your older project wouldn't run with it.

Or, for another even newer project, you wanted to install some other brand new and hot package. Though, that new package requires you to upgrade the above mentioned 1.0 package to 2.0. That is a depedency between packages. Next, the new package will be installed with its newest version. And since the package has a dependency to the older project's package, the 'older' package will be updated, too. This may be alright for your current project. Though, the code of your old project may suffer severely, because something in the package changed and your code starts to throw errors.

So, note this lesson: In order to avoid package dependency issues across the many projects you are working on, always - yes, always - set up a virtual environment to host your project.

Thanks for reading this far. We're not done yet. Just wanted to say that of you wanted to add or correct something, please **help to edit** this post on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/how-to-virtual-env-with-conda.md). Thanks.

## Okay, but why conda?

Now, why should you use conda for ramping up your virtual environment? How does it help? Let me try to explain.

It's probably fair to say that Conda is among the most popular options. Conda not only allows you to manage dependencies across packages. It also installs packages (such as the package manager pip).

Conda is a tool for managing and deploying applications, environments and packages. So, it covers a wider range functoinality.

Well, there are other tools that you could use. Fair point. The above mentioned package manager pip. Or, the environment manager virtualenv. But, the upside of conda is that it is not limited to Python and allows you to manage other programming languages, too. Something that pip doesn't.

Check this article to understand the difference between conda and pip better:
https://stackoverflow.com/questions/20994716/what-is-the-difference-between-pip-and-conda

And find this concise post for learning how to differentiate between anaconda, miniconda, and virtualenv:
https://deeplearning.lipingyang.org/2018/12/23/anaconda-vs-miniconda-vs-virtualenv/

## Create and activate virtual environment

Let's get our hands dirty.

Follow the instructions in the conda docs to install conda. Propably, you may just install Anaconda or Miniconda.
https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

First thing, we **create** a new virtual environment called 'my-new-virt-env' with a current Python version. In my case, I want to install 3.8. Here is the command for your temrinal.
'''
conda create --name my-new-virt-env python=3.8
'''

Once created, we **activate** the new environment so that it is up for use.
'''
conda activate my-new-virt-env
'''

Now, any installed package will be living in the newly created environment. Thus, package dependencies have been decoupled from projects.

As a matter of practicallity and transparency, I suggest to keep naming of project directory and virtual environment same. For the example we have spinned off above, we might need to create a **directory** for our project. So, you can do something like this in terminal.
'''
mkdir my-new-virt-env
cd my-new-virt-env
'''

As you are done with working on the project, **deactivate** the current environment.
'''
conda deactivate
'''

## Manage virtual environment

That's cool. Our environment is up and ready for us to play. But so far, we've only touched the surface of what conda can do. Here are some more commands that can be of good help.

First, get a list of all environments that you have created on your system.
'''
conda info --envs
'''

Then, installing a list of packages into a specified conda environment is done as follows. Note that, if no environment is specified, the current environment is used.
'''
conda install --name my-new-environment pandas
'''

This is how you get a list of all packages in the conda environment.
'''
conda list
'''

And lastly, if you want to part from your created environment, remove an environment with this command.
'''
conda env remove --name my-new-virt-env
'''

There are more cool things you can do with conda, such as cloning or restoring environments. Read more on how to manage environments in conda here:
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
