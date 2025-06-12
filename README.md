# Advanced Linux Commands
Linux Distribution: AWS Linux 
Primarily derived from fedora and centOS linux
## Role of hyphen in permission
If a permission is not defined, it is represented by hyphen i.e hyphen means absent of perrmsission
![Role of hyphen](./images/1.%20Role%20of%20hyphen.png)

## Task One: chmod Command
chmod command is used to modify file or directory permission for a user, group and others. Below steps demostrate chmod command in action.
### Step 1: create new file using touch command
NB: Touch command is used to create new file or update the timestamp of existing file.
![create new file using touch file](./images/2.%20touch%20script.png)

### Step 2: Check the permission details for the file using ls -latr 
![Check the file permission using ls -latr](./images/ls%20-latr%20script.png)

### Step 3: Modify the permission using chmmod +x to include execute permission for all user group.
![modify the permission using chmod +x](./images/4.%20chmod%20+x%20script.png)

### Step 4: Modify the permission using chmod with numeric values to assign different permission level for each user group.
For example: chmod 755 means read, write and execute for user, read and execute for group and others.
![chmod 755](./images/6.%20chmod%20755%20script.png)
![chmod 755 confirmation](./images/7.%20ls%20latr%20script%20confirmation.png)
### Step 5: create another file using touch command
### Step 6: chmod 700 to modify the persmission

### Step 7: ls -latr to confirm permission for user only
![touch notes.txt, chmod 700 , ls -latr ](./images/8.%20touch%20chmod%20700%20and%20ls.png)


## Task Two: chown command
chown command is used to change the ownership of a file or directory for a user or group.

### Step 1: confirm initial ownership of filename.txt using ls-latr
![ls -latr filename.txt](./images/10.png)

### Step 2: change the ownership of filename.txt from ec2-user to jeleel and all users in  jeleel group usin chown jeleel:jeleel and use ls -latr to confirm
![chown jelee:jeleel filename.txt](./images/11%20chown%20filename%20and%20confirmation.png)

## Task Three: Superuser Privilledges
Superuser privilleges is used to perform some sensitive administrative task,because it is not advisable to login as superuser always, the best method to add sudo(super user do) before every command that requires administrative privilleges.
### Step 1: sudo -i to login as root user
![sudo -i for root user login](./images/12.%20sudo%20-i%20switch%20to%20root%20user.png)

## Task Four: User Management in Linux
### Step 1 : Create new user using adduser
Note: This command requires sudo before it because it is an administrative command.
![sudo adduser johndoe](./images/13.%20sudo%20adduser.png)

### Step 2: Grant administrative privillege to the new user using sudo usermod -aG wheel johndoe
![sudo usermod -aG wheel jogndoe](./images/14.%20sudo%20usermod-%20add%20sudo%20priviledge.png)

### Step 3: Login as new user johndoe using su johndoe and cd /home/johndoe
![su johndoe](./images/15.%20su%20johndoe.png)
![cd /home/johndoe](./images/16.%20cd%20home%20johndoe.png)

### Step 4: Changing user password using sudo passwd johndoe
![sudo passwd johndoe](./images/17.%20sudo%20passwd%20johndoe.png)

### Step 5: Login with the johndoe user with the new password
![su johndoe](./images/18.%20su%20johndoe%20with%20new%20password.png)

### Step 6: Creating group using sudo groupadd developers
Note: Group is an abstract collection of users with similar role and task.
![sudo groupadd developers](./images/19.%20sudo%20groupadd%20developers.png)

### Step 7: Adding user to the created group using usermod command
![sudo usermod -aG developers johndoe](./images/19.%20sudo%20groupadd%20developers.png)

### Step 8: Verify group membership using id johndoe
![id johndoe](./images/20.%20id%20johndoe.png)


### Step 9: Deleting a user using userdel johndoe and confirm deletion using id johndoe
![sudo userdel johndoe](./images/21.%20sudo%20userdel%20johndoe.png)

## Task Five: Grant  group ownership of a directory.
ownership of a directory or file can be granted to a user or group using chown command.

### Step 1: Grant developer group ownership of to directory
![sudo chwon :developers path/to/directory](./images/22.%20chown%20directory.png)

### Step 2:Grant Read/Write permission to the group
![sudo chmod g+rw /path/to/directory](./images/23.%20chmod%20grw.png)

## Task Six: User and Group management
### Step 1: Create group named devops using groupadd command, create 5 users and add each user to the devops group
![sudo groupadd deveops](./images/25.%20group%20devops%20and%20useradd.png)

### Step 2: Create /home directory for each user (Mary, mohammed, ravi, tunji, sofia)
![mkdir mary, cd /home](./images/26.%20su%20mary%20mkdir%20mary.png)

![mkdir mohammed, cd /home](./images/27.%20su%20mohammed%20mkdir%20mohammed.png)


![mkdir ravi, cd /home](./images/28.%20su%20ravi%20mkdir%20ravi.png)

![mkdir tunji, cd /home](./images/29.%20su%20tunji%20mkdir%20tunji.png)

![mkdir sofia, cd /home](./images/30.%20su%20sofia%20mkdir%20sofia.png)

### Step 3: Add Mary, Mohammed, ravi, Tunji and Sofia to devops group
![chown :devops mary](./images/32.%20chown%20devops%20mary.png)

![chown :devops mohammed](./images/33.%20chown%20devops%20mohammed.png)

![chown :devops ravi](./images/34.%20chown%20devops%20ravi.png)

![chown :devops tunji](./images/35.%20chown%20devops%20tunji.png)

![chown :devops sofia](./images/31.%20chown%20devops%20sofia.png)








