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
 
# Docker Concepts

1. **Docker**: It is a platform that is used to build, run and ship applications.
2. Eg. 2 completely different apps with completely different dependencies can run on same system using it. Eg. App 1 (uses Node 14 and Mongo 4) and App 2 (uses Node 9 and Mongo 3)
3. If the use of an app (built using docker) is done, it can be compeletely removed from the system without affecting other apps and their dependencies.
4. Container - An isolated env for running an application.
5. Virtual Machine - An abstraction of a machine (physical hardware). Eg On a Mac - 2 virtual machine can be present -> a. Windows b. Linux
6. VMs can be created using a HyperVisor software like VirtualBox or VMware or Hyper-v(windows only)
7. Disadvantages with Virtual Machines are:
    <ul>
      <li>Each Virtual Machine needs a fully installed OS</li>
      <li>Slow to start</li>
      <li>resource intensive</li>
     </ul>
8. Advantages with Containers are:
    <ul>
      <li>Allow running multiple apps in isolation</li>
      <li>Are lightweight</li>
      <li>Use OS of the Host</li>
      <li>Start Quicklyt</li>
      <li>Needs less hardware resources</li>
     </ul>
9. Docker Architecture:
- On a windows pc -> Windows + Linux containers can run (windows 10 contain linux kernel)
- On a Linux system -> Linux containers can run
- On a Mac system -> Linux container can run using Linux VM
