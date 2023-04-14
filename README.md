## Login in AWS
* Once credentials are recieved, on GitBash move credentials to the .ssh directory.
* We now use these credentials to log into AWS as shown below.
<img width="1277" alt="Screenshot 2023-04-14 at 18 30 35" src="https://user-images.githubusercontent.com/129948378/232116313-46194661-648b-4f71-ad1c-45ce4e080fa8.png">



Using `cd .ssh` to access the directory, `ls` to see the contents of the directory, then `cat <filename>.pem` to read the file.

Once recieving the .pem file, we will open it via Notepad to allow us to progress to the next step.
![image](pem.png)

After copying the file we use `nano <filename>.pem` to create a new `.pem` file where we will copy and paste from the notepad file to our secure `.ssh` directory. All the while deleting the copy in Downloads.  We can see what it will look like once we enter the nano code, and copy and paste the pem file within the nano.
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

# How to set up an EC2 instance

Here are the steps to set up an EC2 instance on AWS.

##### Basic startup steps

First head over to the AWS and login.
Find and then select the option to Launch a Virtual Machine. 


##### Select the feature for your EC2 instance

First you input a name for your EC2 instance, make sure to use a good naming 
convention


Then you select an AMI - chose ubuntu


Leave the instance type as t2.micro

Select a keypair - if you don't have one then create one.

Under 'Network Settings' makesure SSH traffic is from your "My IP" address and select the checkbox 
to allow HTTP traffic from the internet.


Whilst in the 'Network Settings' section, click edit and ensure you name your security with similar naming convention 
as earlier.


keep the other features as is for now and the click 'Launch Instance'.


##### Launch Instance

Once your ec2 instance has been initialized then navigate to your running instance, select the checkbox 
and press connect. 

![](Screenshot 2023-04-13 at 17.29.03.png)

Make sure you're in the "SSH Client" tab and then head over to Git Bash App.

When in Git Bash, go to the folder where your .pem file is saved, then follow the instructions from aws.



Once you are connected to aws from your Git bash the command line will start with something like


# How to amend a security group in AWS

Once you have launched your EC2 instance with a security group you can, if like, amend the security group.

- To do this, check the box for the instance. In the panel underneath, navigate to the security tab.
Once on the security tab, click on the link to the security group.

![](Screenshot 2023-04-13 at 17.43.23.png)


- Then click on "Edit Inbound Rules"

![](Screenshot 2023-04-13 at 17.43.53.png)

At this point you can add new inbound rules and/or delete rules. Once the necessary changes have been made, 
click on "Save Rules"

![](Screenshot 2023-04-13 at 17.44.31.png)


###  Automate the process: 
- bash scripting - when a scripting file is created it should end with `.sh`

- we can create this file using `touch "file_name.sh"`

- we can then write to it - `sudo nano script.sh` and add the following text.
, to save and exit press CTRL+X and then Y for yes.
```
#!/bin/bash
# update
sudo apt update -y
# upgrade
sudo apt upgrade -y
# install Nginx
sudo apt install nginx -y
# restart Nginx
sudo systemctl restart nginx
# enable Nginx
sudo systemctl enable nginx
```

- we then need to make the file executable with `sudo chmod +x "file_name"`

- Then we can run the script: `sudo ./"file_name"` and our script should automate the 
commands.

 
