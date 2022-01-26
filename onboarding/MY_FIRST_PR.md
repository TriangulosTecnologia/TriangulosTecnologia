# My First PR

### Hi, people! How are you doing? In this docs, I will write about the steps that I did to make my first PR. If any step is wrong or shallow, please give feedback. I'm counting on you. An observation: I will try to make the steps separate from the OS that I used.

## 1. Required software

- Git;
- Code editor of your choice.

## 2. Steps

### 1. Clone the repository using Git and create a new branch

#### For the first part, it is necessary to clone the repository where you will work on your local PC. For this, open Git and type the following command:

#### *git clone "repository of your choice"* 

#### After this, you will create a new branch to work in the project. For this, you will use:

#### *git checkout -b "name of the issue"*

### 2. Start working in the project

#### Self-explanatory. :D

### 3. Preparing for PR

#### After the modifications are made, it's time for prepare to PR. Go to the root of your project, open Git and type this:

#### *git status*

#### This command will highlight the files that were modified by you. If you want theses files on the PR, type:

### *git add "each one of the files*

### After this, you have to save the project. For this, type:

#### *git commit -m "commentary about the update"*

#### This command saves the project and keep a commentary about the contents of the update. Finally, we have to upload the local repository. Type:

#### *git push origin HEAD*

### 4. Doing the PR

- Finally, the final step. Now, open Github.com, log in with your user and select the branch with your commit;
- Click on Pull request;
- Select the branch where you would like to merge your changes into and leave a description about it;
- Click on Create Pull Request;

#### It's done. If your pull request is accepted, you can merge your modifications into the repository.

#### References:

https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request
