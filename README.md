## Login in AWS


![image](https://user-images.githubusercontent.com/129948378/231733802-fadc3a43-1758-4e4c-affd-be03aabc6910.png)Once credentials are recieved, on GitBash move credentials to the .ssh directory.
We now use these credentials to log into AWS as shown below.
<img width="561" alt="Screenshot 2023-04-13 at 11 35 05" src="https://user-images.githubusercontent.com/129948378/231733432-0c5196c6-b86a-4766-94df-bd4421442027.png">


Using cd .ssh to access the directory, ls to see the contents of the directory, then cat <filename>.pem to read the file.

Once recieving the .pem file, we will open it via Notepad to allow us to progress to the next step.
  
 mv file_name_to_move(mateusz...) location_where_you_want_to_move_it (~/.ssh)

cd .ssh access .ssh file

nano tech221.pem open up notepad and paste KEY

ctrl + s (save)   &   ctrl + x (close)

cat tech221.pem to check changes in tech221.pem file

After copying the file we use nano <filename>.pem to create a new .pem file where we will copy and paste from the notepad file to our secure .ssh directory. All the while deleting the copy in Downloads. We can see what it will look like once we enter the nano code, and copy and paste the pem file within the nano.



After you have pasted the correct information, we ctrl x, then we press y to confirm our selection. After this we press Enter to finalize everything and to close the nano window. This will save the file withour pasted information within the .ssh folder.
