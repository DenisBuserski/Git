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




  


<details>
<summary><h2>Install Git</h2></summary>
<br>
     
1. To install Git visit - https://git-scm.com/
2. Follow the below steps for the installation

     ![step-1](git-steps/g-1.png) 
     ![step-2](git-steps/g-2.png)

     ![step-3](git-steps/g-3.png)

     ![step-4](git-steps/g-4.png)

     ![step-5](git-steps/g-5.png)
 
     ![step-6](git-steps/g-6.png)

     ![step-7](git-steps/g-7.png)

     ![step-8](git-steps/g-8.png)

     ![step-9](git-steps/g-9.png)

     ![step-10](git-steps/g-10.png)

     ![step-11](git-steps/g-11.png)

     ![step-12](git-steps/g-12.png)

     ![step-13](git-steps/g-13.png)

     ![step-14](git-steps/g-14.png)

     ![step-15](git-steps/g-15.png)

     ![step-16](git-steps/g-16.png)
     
     ![step-17](git-steps/g-17.png)
</details>


##

<details>
<summary><h2>Git commands(Windows)</h2></summary>
<br>

Before following the below commands you would need to set Git with your GitHub profile. You can check [here](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git) how to do it.


1. Create a folder on your Desktop named "test"

2. Right click on it and select "Open Git Bash here"

   ![gc-2](git-commands/gc-2.png)

3. Open the folder "test"

4. In the Git console write the command
   ```
   git init
   ```
   This command creates a Local repository on your PC
   
   ![gc-4](git-commands/gc-4.png)

5. Create "file-1.txt" in the "test" folder 
   ```
   touch file-1.txt
   ```
   ![gc-5](git-commands/gc-5.png)

6. Check the status of our Local repository
   ```
   git status
   ```
   ![gc-6](git-commands/gc-6.png)

   From the result we got, it can be seen that we don't have any commits and we have 1 untracked file.

7. As mentioned in the result we got from the previous point we need to use:
   ```
   git add file-1.txt
   ```
   ![gc-7](git-commands/gc-7.png)

8. Check the status 
   ```
   git status
   ```
   
   ![gc-8](git-commands/gc-8.png)

9. Commit the changes
   ```
   git commit -m "Add text file"
   ```
   ```
   git commit -m "[Message]"
   ```

   ![gc-9](git-commands/gc-9.png)
   
   From the above message we can see that we have added a new commit with a message "Add text file" and we have changed 1 file(file-1.txt)

10. Check the status
    ```
    git status
    ```
    
    ![gc-10](git-commands/gc-10.png)

    When we see the above message, that means we are ready to the push the changes and add them to the Remote repository.

11. Add some text to file-1.txt
    ```
    echo "Sofia" >> file-1.txt
    ```

    ![gc-11](git-commands/gc-11.png)

12. You can clear your console using
    ```
    clear
    ```

13. After adding text to file-1.txt, check the status
    ```
    git status
    ```

    ![gc-13](git-commands/gc-13.png)

    From the above message we can either prepare our changes for commit or discard the changes we have made.
    If we want to restore the previous state of the file we have to use:
    ```
    git restore file-1.txt
    ```

    If we want to keep the changes we made and prepare them for commit we have to use:
    ```
    git add file-1.txt
    ```
    With this command we can add 1 file at a time, but what if we have multiple... 

14. Add 2 more files to the "test" folder
    ```
    touch file-2.txt
    touch file-3.txt
    ```
    ![gc-14](git-commands/gc-14.png)

15. Check the status
    ```
    git status
    ```
    ![gc-15](git-commands/gc-15.png)

16. Add all files at once
    ```
    git add .
    ```
    ![gc-16](git-commands/gc-16.png)

17. Check the status
    ```
    git status
    ```
    ![gc-17](git-commands/gc-17.png)

18. Commit the changes
    ```
    git commit -m "Added 2 new files and changed file-1.txt"
    ```
    ![gc-18](git-commands/gc-18.png)

19. Check the status
    ```
    git status
    ```
    ![gc-19](git-commands/gc-19.png)

20. Remove file-3.txt
    ```
    rm -i file-3.txt
    ```
    Since we are using "-i", we will be asked whether we want this file to be deleted. 
    ![gc-20](git-commands/gc-20.png)

21. Check the status
    ```
    git status
    ```
    ![gc-21](git-commands/gc-21.png)

22. Prepare everything for commit and check the status
    ```
    git add .
    git status
    ```
    ![gc-22](git-commands/gc-22.png)

23. Commit
    ```
    git commit -m "Deleted file-3.txt"
    ```
    ![gc-23](git-commands/gc-23.png)

24. Check the history of your commits
    ```
    git log
    ```
    ![gc-24](git-commands/gc-24.png)

25. Connect our Local repository with the one in GitHub
    
    We need a repository in our GitHub. To create one follow the steps below:

    Step 1
    
    <kbd> ![25-1](git-commands/gc-25-1.png) </kbd>

    Step 2
    
    <kbd> ![25-2](git-commands/gc-25-2.png) </kbd>

    Step 3

    <kbd> ![25-3](git-commands/gc-25-3.png) </kbd>

    I have created this [one](https://github.com/DenisBuserski/test).

    Copy the URL of the repository and use the following command
    ```
    git remote add origin [URL]
    ```
    ```
    git remote add origin https://github.com/DenisBuserski/test
    ```
    ![25-4](git-commands/gc-25-4.png)

    We need to move to our main branch
    ```
    git checkout -b main
    ```
    ![25-5](git-commands/gc-25-5.png)

    After that we need to fetch the data from it
    ```
    git fetch origin main
    ```
    ![25-6](git-commands/gc-25-6.png)

    Rebase
    ```
    git rebase origin/main
    ```
    ![25-7](git-commands/gc-25-7.png)

    Push our changes
    ```
    git push -u origin main
    ```
    ![25-8](git-commands/gc-25-8.png)

    After that you will see "file-1.txt" and "file-2.txt" in your GitHub repository.

26. There was a change in file-2.txt, which was not done by us. In this case we would need to take those changes on our side.

    Modify file-2.txt directly from GitHub. Follow bellow to see how:

    <kbd> ![gc-26-1](git-commands/gc-26-1.png) </kbd>

    <kbd> ![gc-26-2](git-commands/gc-26-2.png) </kbd>

    <kbd> ![gc-26-3](git-commands/gc-26-3.png) </kbd>

    After the file was changed we will pull those changes on our side:
    ```
    git pull
    ```
    This command takes the latest changes.
    
    ![gc-26-4](git-commands/gc-26-4.png)

    Now when we have pulled the changes. You can check if file-2.txt is changed on our side:
    ```
    cat file-2.txt
    ```
    ![gc-26-5](git-commands/gc-26-5.png)

27. Modify file-2.txt from GitHub and we will use 
    ```
    git fetch
    ```
    so we can see what the difference between "pull" and "fetch" is.

    ![gc-27-1](git-commands/gc-27-1.png)

    ```
    git diff main..origin/main
    ```
    ![gc-27-2](git-commands/gc-27-2.png)

    We can see what changes were made to the file, before we pull those changes on our Local repository

    ```
    git pull
    ```
    ![gc-27-3](git-commands/gc-27-3.png)

    ```
    git status
    ```
    ![gc-27-4](git-commands/gc-27-4.png)

28. What if we don't have the repository on our machine?
    Create a new folder on you Desktop named "Projects", right click on it "Open Git Bash Here".
    ```
    git clone [URL]
    ```
    ```
    git clone https://github.com/DenisBuserski/test
    ```
    ![gc-28](git-commands/gc-28.png)



<h4> You acan check here a grafical explanation of most of the commands we used. </h4>

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

Following we already know the Git commands:

![p-5](git-with-intellij/p-5.png) 

![p-6](git-with-intellij/p-6.png) 

![p-7](git-with-intellij/p-7.png) 

![p-8](git-with-intellij/p-8.png) 

Someone made some changes... Lets see them... 

![p-9](git-with-intellij/p-9.png) 

We don't have this project on our PC...

<kbd> ![p-10](git-with-intellij/p-10.png) </kbd>

<kbd> ![p-11](git-with-intellij/p-11.png) </kbd>

![p-12](git-with-intellij/p-12.png) 

![p-13](git-with-intellij/p-13.png) 

</details>


##

<details>
<summary><h2>How to use GitHub Desktop (In progress)</h2></summary>
<br>

You can download GitHub Desktop from [here](https://desktop.github.com/)

</details>

