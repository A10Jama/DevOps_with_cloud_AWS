image
Once credentials are recieved, on GitBash move credentials to the .ssh directory.
We now use these credentials to log into AWS as shown below.
image

Using cd .ssh to access the directory, ls to see the contents of the directory, then cat <filename>.pem to read the file.

Once recieving the .pem file, we will open it via Notepad to allow us to progress to the next step. image

After copying the file we use nano <filename>.pem to create a new .pem file where we will copy and paste from the notepad file to our secure .ssh directory. All the while deleting the copy in Downloads. We can see what it will look like once we enter the nano code, and copy and paste the pem file within the nano.

image

After you have pasted the correct information, we ctrl x, then we press y to confirm our selection. After this we press Enter to finalize everything and to close the nano window. This will save the file withour pasted information within the .ssh folder.
