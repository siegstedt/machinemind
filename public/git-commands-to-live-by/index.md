# Git Commands to Live By


Git is an essential tool for programmming. If you want to get deeper involved in coding, better be prepared to get familiar with some of the most vital commands. Here is a short summary broken down to scenarios.

<!--more-->

Help to **improve this post** on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/git-commands-to-live-by.md). Thank you for your contribution.

## Create a new repository from a local folder

For the first case, we assume that you have some content in a folder on your local machine and you want to push to a GitHub repository. For that purpose you have already created an empty repository on GitHub. E.g. I have called mine 'machinemind'.

Well, the local folder is not even a git repo yet. So we first need to intitialize the folder as an empty repository.Below examplary code is working with the machinemind repo as a case study.

```
cd projects/machinemind
git init
```

Now the 'machinemind' folder carries a .git folder. As we said, it is empty for now. So let's give some signal to Git that we want to add our content to the repository. 

```
git add .
git commit -m "first commit"
```

Now, Git knows what changes we want to commit, we need to push them to the system. Before we call 'push', we need to specify whehre to push it to. That requires us to first set a branch on which our workstream is supposed to sit. And secondly, the definition of origin as an address for our remote machine.

```
git branch -M main
git remote add origin https://github.com/siegstedt/landlord.git
git push -u origin main
```

That's it. The content of your folder is up there in the GitHub hosted repository.

## Clone a repository to a local folder

Second case: You want to work on some repository that is hosted on GitHub. Therefore, you want to bring it on your local machine. The process is called cloning. And here is how you do it.

The terminal commands we will use here are very brief and simple. First, we navigate to folder to which the repository is to be added to. And then we call the 'git clone' command on the url of the repository.

Again, I will work with the 'machinemind' repository that I have created above.

```
cd projects
git clone https://github.com/siegstedt/machinemind
```

## Pull newest status

For the third scenario, we want to assume that you have a repo on your local machine and you are co-working on it together with your team mates.

To make sure that you are having the latest version of the repository on your machine, you should pull all new changes before you start working on the code yourself.

Here are the commands that you could use for the machinemind repo.

```
cd projects/machinemind
git pull
```

First, we navigated to the directory. Then, we just called the 'git pull' command.

Note that there may be scenarios where you want to work on a different branch then the original branch, for instance because you want to develop and test a new feature. In that case, you can tweak the pull commands. Here is a link in which such scenarios are well explained: https://www.w3docs.com/learn-git/git-pull.html

## Push the changes

Alright! Say, you've synced your repository and added a new feature. Now, you want to play it back to the original repository.

We're already familiar with parts of the commands, namely the 'add' and 'commit'. The only addition we need to make on our terminal is a line on push the commit.

```
cd projects/machinemind
git add .
git commit -m 'adding a new feature'
git push
```

## Ignore files from commit

Sometimes we run into scenarios where we don't want to upload all files in your local folder to the GitHub repository. That may for instance be because these are huge data files, or sensitive identity data, etc.

But how do you tell Git not to upload these files - how to make Git ignore these files?

Navigate to the folder and create a .gitignore file.

```
cd projects/machinemind
touch .gitignore
```

Open the .ignore file and edit it as per liking. You can put folder names, file names, or glob patterns.

For inspiration and guidance, find these two links:
- A collection of .gitignore template: https://github.com/github/gitignore
- Some common gitignore configurations: https://gist.github.com/octocat/9257657

## Further ressources

https://docs.github.com
https://git-scm.com

