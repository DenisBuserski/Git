# How to use Git


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
<summary><h2>Connect Git with GitHub</h2></summary>
<br>

hey
hey
hey
</details>

##

<details>
<summary><h2>Git commands</h2></summary>
<br>

1. Create a folder on your Desktop named "test"

2. Right click on it and select "Git Bash Here"

   ![1](git-commands/w-1.png)

4. Open the folder "test"

5. In the Git console write the command
   ```
   git init
   ```
   This command created a Local repository on your PC
   
   ![2](git-commands/w-2.png)

5. Create "file-1.txt" in the "test" folder 
   ```
   touch file-1.txt
   ```
   ![3](git-commands/w-3.png)

6. Lets check the status of our Local repository
   ```
   git status
   ```
   ![4](git-commands/w-4.png)

   From the result we got, it can be seen that we don't have any commits and we have 1 untracked files.

7. As mentioned in the result we got from the previous point we need to use:
   ```
   git add file-1.txt
   ```
   ![5](git-commands/w-5.png)

8. Lets check the status again
   ```
   git status
   ```
   
   ![6](git-commands/w-6.png)

9. Commit the changes
   ```
   git commit -m "Add text file"
   ```
   ```
   git commit -m "[Message]"
   ```

   ![7](git-commands/w-7.png)
   
   From the above message we can see that we have added a new commit call "Add text file" and we have changed 1 file(file-1.txt)

10. Check the status
    ```
    git status
    ```
    
    ![8](git-commands/w-8.png)

    When we see the above message, that means we are ready to the push the changes and add them to the Remove repository.

11. Add some text to file-1.txt
    ```
    echo "Sofia" >> file-1.txt
    ```

    ![9](git-commands/w-0.png)

12. You can clear your console using
    ```
    clear
    ```

</details>
