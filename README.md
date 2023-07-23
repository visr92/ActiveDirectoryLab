<h1>File permissions in Linux</h1>


<h2>Description</h2>
This project consists of demonstrating how to update file permissions for certain files and directories within "projects" directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks:

<br />


<h2>Language</h2>

- <b>SQL</b> 


<h2>Environment Used </h2>

- <b>Linux/Bash</b> 

<h2>Project Walk-Through:</h2>

<p align="center">
<b>Check file and directory details:</b> <br>
                                    
The following code demonstrates how I used Linux commands to determine the existing permissions set for a specific directory in the file system.
<p align="center"> 
<img src="https://i.imgur.com/6hU4DxJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br>
<br />
<p align=” justify”>
The first line of the screenshot displays the command I entered, and the other lines display the output. The code lists all contents of the projects directory. I used the ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named drafts, one hidden file named .project_x.txt, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.
<br />
<br />
<p align="center">
<b>Change file permissions:</b>  <br/>
  
I determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined project_k.txt must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:
<p align="center">
<img src="https://i.imgur.com/qZvLROp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br>
<br />
<p align=” justify”>
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The chmod command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the project_k.txt file. After this, I used ls -la to review the updates I made.
<br />
<br />
<p align="center">
<b>Change directory permissions:</b> <br/>

I've decided I only wants the researcher2 user to have access to the drafts directory and its contents. This means that no one other than researcher2 should have execute permissions.

The following code demonstrates how I used Linux commands to change the permissions:

<p align="center">
<img src="https://i.imgur.com/ohAqCTc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I previously determined that the group had execute permissions, so I used the chmod command to remove them. The researcher2 user already had execute permissions, so they did not need to be added.
<br />
<br />
<p align="center">
<b>Summary</b> <br/>
I changed multiple permissions to match the level of authorization I wanted for files and directories in the projects directory to have. The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories.
<br />
<br />
