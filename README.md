# How to use Git


## Overview

- Software Configuration Management(SCM) = Version Control(VS/VCS)
- Software principle
- When several programmers write code, the codes of which are then combined into 1 project. VC allows this to be more balanced and controls the whole process
- Keeps history of the made changes
- Conflict - When 2 people work on the same code and correct the same line
- Repository
  - The code repository used in a project
  - Project code    
- Open source code - Everyone can see the code
- GitHub - If you are not added as a collaborator, you cannot make pull requests

| Git        | GitHub  | Git Bash |
| ---------- | ------- | -------- |
| Version control | Portal | Client we use to upload code to GitHub |
| Methodology | | |


There are 2 types of Source-Control Systems 

| Distributed Source-Control System | Centralized Source-Control System |
| --------------------------------- | --------------------------------- |
| Git | SVN |
| 2 types of repository | |
| Remote - The main project from which the files are downloaded | Only 1 repository (Remote repository) |
| Local - Everyone involved in this project has 2 repositories | No Local repository |
| In case of conflict, the individual programmer can download the changes in his repository that the other has made and make the appropriate changes | Almost always we get conflicts and they are very hard to fix |






##

<details>
<summary><h2>Git commands</h2></summary>
<br>

Before following the below commands you would need to set Git with your GitHub profile. You can check [here](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git) how to do it.

1. Create a folder on your Desktop named "test"<br>
   Open `Git Bash` on your Desktop and create folder `test` with the `mkdir test` command.
   ![step_1](git-commands/step_1.png)
2. Move to the `test` folder
   ```
   cd test
   ```
   ![step_2](git-commands/step_2.png)
3. In the Git console write the command
   ```
   git init
   ```
   This command initializes a new, empty repository. Git creates a new `.git` directory in your project. Using the `ls -a` command we can see the mentioned directory.
   ![step_3](git-commands/step_3.png)
4. Use the `clear` command to clear the console
5. Create `file-1.txt` in the `test` folder 
   ```
   touch file-1.txt
   ```
   ![step_5](git-commands/step_5.png)
6. Check the status of your Working directory
   ```
   git status
   ```
   ![step_6](git-commands/step_6.png)
   From the result, it can be seen that you don't have any commits and have 1 untracked file.
7. Move the file to the Staging area
   ```
   git add file-1.txt
   ```
8. Check the status
   ![step_8](git-commands/step_8.png)

9. Commit the changes to you Local repository
   ```
   git commit -m"[Message]"
   ```
   ```
   git commit -m"Created file-1.txt"
   ```
   ![step_9](git-commands/step_9.png)
10. Check the status
    ![step_10](git-commands/step_10.png)
    When you see the above message, that means you are ready to the push the changes and add them to the Remote repository.
11. Add some text to file-1.txt
    ```
    echo "Sofia" >> file-1.txt
    ```
12. Check the status
    ![step_12](git-commands/step_12.png)
    From the above message you can either prepare your changes for commit or discard the changes you have made.
    If you want to restore the previous state of the file you have to use:
    ```
    git restore file-1.txt
    ```
    If you want to keep the changes you made and prepare them for commit you have to use:
    ```
    git add file-1.txt
    ```
    With this command you can add 1 file at a time, but what if you have multiple...
13. Add 2 more files to the "test" folder
    ```
    touch file-2.txt
    touch file-3.txt
    ```
14. Check the status
    ```
    git status
    ```
    ![step_14](git-commands/step_14.png)
15. Add all files at once
    ```
    git add .
    ```
    ![step_15](git-commands/step_15.png)
16. Check the status
    ![step_16](git-commands/step_16.png)
17. Commit the changes
    ```
    git commit -m"Added 2 new files and changed file-1.txt"
    ```
18. Check the status
    ![step_18](git-commands/step_18.png)
19. Remove file-3.txt
    ```
    rm -i file-3.txt
    ```
    Since you are using `-i`, you will be asked whether you want this file to be deleted. 
    ![step_19](git-commands/step_19.png)
20. Check the status
    ![step_20](git-commands/step_20.png)
21. Prepare everything for commit and check the status
    ```
    git add .
    git status
    ```
    ![step_21](git-commands/step_21.png)
22. Commit
    ```
    git commit -m "Deleted file-3.txt"
    ```
    ![step_22](git-commands/step_22.png)
23. Check the history of your commits
    ```
    git log
    ```
    ![step_23](git-commands/step_23.png)
24. Connect your Local repository with the one in GitHub




<br>

25. Connect your Local repository with the one in GitHub
    
    You need a repository in your GitHub. To create one follow the steps below:

    Step 1
    
    <kbd> ![25-1](git-commands/gc-25-1.png) </kbd>

    Step 2
    
    <kbd> ![25-2](git-commands/gc-25-2.png) </kbd>

    Step 3

    <kbd> ![25-3](git-commands/gc-25-3.png) </kbd>

    Copy the URL of the repository and use the following command:
    ```
    git remote add origin [URL]
    ```
    ```
    git remote add origin https://github.com/DenisBuserski/test
    ```
    ![25-4](git-commands/gc-25-4.png)

    Move to your main branch:
    ```
    git checkout -b main
    ```
    ![25-5](git-commands/gc-25-5.png)

    Fetch the data from it:
    ```
    git fetch origin main
    ```
    ![25-6](git-commands/gc-25-6.png)

    Rebase:
    ```
    git rebase origin/main
    ```
    ![25-7](git-commands/gc-25-7.png)

    Push your changes:
    ```
    git push -u origin main
    ```
    ![25-8](git-commands/gc-25-8.png)

    After that you will see "file-1.txt" and "file-2.txt" in your GitHub repository.

26. There was a change in file-2.txt, which was not done by you. In this case you would need to take those changes on your side.

    Modify file-2.txt directly from GitHub. Follow bellow to see how:

    <kbd> ![gc-26-1](git-commands/gc-26-1.png) </kbd>

    <kbd> ![gc-26-2](git-commands/gc-26-2.png) </kbd>

    <kbd> ![gc-26-3](git-commands/gc-26-3.png) </kbd>

    After the file was changed you will pull those changes on your side:
    ```
    git pull
    ```
    This command takes the latest changes.
    
    ![gc-26-4](git-commands/gc-26-4.png)

    Now when you have pulled the changes. You can check if file-2.txt is changed on your side:
    ```
    cat file-2.txt
    ```
    ![gc-26-5](git-commands/gc-26-5.png)

27. Modify file-2.txt from GitHub and use: 
    ```
    git fetch
    ```
    Now you wil see what the difference between "pull" and "fetch" is.

    ![gc-27-1](git-commands/gc-27-1.png)

    ```
    git diff main..origin/main
    ```
    ![gc-27-2](git-commands/gc-27-2.png)

    You can see what changes were made to the file, before you pull those changes on your Local repository.

    ```
    git pull
    ```
    ![gc-27-3](git-commands/gc-27-3.png)

    ```
    git status
    ```
    ![gc-27-4](git-commands/gc-27-4.png)

28. What if you don't have the repository on your machine?
    Create a new folder on your Desktop named "Projects", right click on it "Open Git Bash here".
    ```
    git clone [URL]
    ```
    ```
    git clone https://github.com/DenisBuserski/test
    ```
    ![gc-28](git-commands/gc-28.png)



<h3> You can check here a grafical explanation of some of the commands we used. </h3>

<kbd> ![0](git-commands/git-simple-workflow.png) </kbd>
    
</details>


##

<details>
<summary><h2>How to use Git with Intellij</h2></summary>
<br>

Create a new repository on GitHub

<kbd> ![p-1](git-with-intellij/p-1.png) </kbd>

Create a new project in IntelliJ

![p-2](git-with-intellij/p-2.png) 

Select "Terminal"

![p-3](git-with-intellij/p-3.png) 

![p-4](git-with-intellij/p-4.png) 

Following you already know the Git commands:

![p-5](git-with-intellij/p-5.png) 

![p-6](git-with-intellij/p-6.png) 

![p-7](git-with-intellij/p-7.png) 

![p-8](git-with-intellij/p-8.png) 

Someone made some changes... Lets see them... 

![p-9](git-with-intellij/p-9.png) 

You don't have this project on our PC...

<kbd> ![p-10](git-with-intellij/p-10.png) </kbd>

<kbd> ![p-11](git-with-intellij/p-11.png) </kbd>

![p-12](git-with-intellij/p-12.png) 

![p-13](git-with-intellij/p-13.png) 

</details>


##

<details>
<summary><h2>Additional information</h2></summary>
<br>

TEST

</details>


