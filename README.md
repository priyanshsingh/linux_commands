# Linux Commands
1. Shell in linux is a CLI that is used to control the OS. eg iterm, terminal in windows, cmd
2. How does os knows the commands like ```git```, ```python3``` etc. They are executable files located in system -> their path is set in the environment variables
3. ```where``` command can be used to find the location of these exec files.
4. List all items in a folder - ```ls``` (list command) (dir in windows)
5. Make Directory - ```mkdir```. Eg creating directory inside a directory -> ```mkdir src/componnts```
6. Making a middle directory between two existing directories. We use-> ```mkdir -p parent_folder/middle_folder/child_folder```
7. Change directory - ```cd```
8. Remove directory - ```rmdir```
9. To reveal a path in file explorer - ```open``` cmd is used (```start .``` in windows)
10. ```ls -a``` -> shows all files including hidden files
11. ```ls -l``` -> detailed information of all the directories
12. ```ls -al``` -> combined command for both.
13. ```ls -R``` ->recursivly lsting all the files.
14. Path variables are stored in the ```zprofiles``` of the zsh cli used by mac
15. ```pwd``` -> print workig directory
16. ```cat``` -> cmd used to print the content of any file eg a js file's code
17. ```cat > hello``` then in next line "my name is Priyansh" -> no such file as hello exists so it gets created with the text contained in it.
18. merging contents of two files one.txt and two.txt -> ```cat one.txt two.txt > new.txt```
19. ```cd .``` will stay in that dir
20. ```cd ..``` will go to previous directory
21. ```man``` command is used to get the deails of a particular command for eg. ```man echo```, this givrs the details of all the information of the ```echo```command
22. ```tr```command is used to Translate the text of a given file to another format. For example to convert text into uppercase: ```cat file.txt | tr a-z A-Z > upper.txt```
23. In the upper example the optput of the first command acts as input for the second command. The Greater than sign ```>``` is for redirection where you the generated output to a particular file.
24. For chaining multiple commands, one after the another you can use ```\``` for the same. Eg ```cat file.txt \ cd ..```
25. Copy command is ```cp```
26. Move command is ```mv```. Eg ```mv file.txt hello``` this will move the file file.txt to the hello directory
27. Using the ```mv``` command we can rename the files as well, for eg. ```mv file.txt hello.txt```
28. Removing a file, we can use the ```rm``` command. For eg ```rm file.txt```
29. 
 
