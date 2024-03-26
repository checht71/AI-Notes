## SSH Command:
````sh
ssh [OPTIONS] [USER@]:HOST
````



## Setup
Checking for ssh
`ls -al ~/.ssh`

Create a new config file:
`touch /.ssh/config`

Edit config file:
`vim ~/.ssh/config`

Add new ssh key:
`ssh-add keyfile.pem`

Add security to your new key file (always do this):
````
chmod 600 keyfile.pem
````

```bash
Host Host
HostName 11.235.1325.22
User abcdefg
Port 22
```

Check GPU resources:
`nvidia-smi`

Keep in mind that the packages and extensions that you have on your machine might not sync with the other one.

This process is the same for every computer

Get GitHub repos setup so that you can easily install the dependencies for your code.

## Sites that use SSH

#### Azure:
See [[Azure Guide]]
You can use thousands of nodes in Azure and set up cloud databases, storage, virtual machines, etc.

There are virtual machines with anaconda set up and installed:
`Data Science Virtual Machines`

### WandB
USE WANDB TO SAVE YOUR PERFORMANCE DATA!!! Save the models themselves elsewhere if you need to.

### Github
Github can use SSH for easily uploading and cloning your files to repos.

### Lamda Cloud
Lambda cloud allows you to access virtual machines via ssh. You can also upload files to the virtual machines via Filezilla using only SSH.
[Here's the tutorial on SSH for Lambda Cloud](https://lambdalabs.com/blog/getting-started-with-lambda-cloud-gpu-instances). Once you create an instance, the site will generate a string for you to copy and paste into your console to ssh in. It will look something like this:

```bash
ssh ubuntu@150.136.248.77
```

## Using FileZilla on Lambda Cloud
1. Open "Site Manager" under file
2. Select SFTP Protocol.
3. In "host" copy and paste the IP address from the ssh.
4. In "username" copy and paste the username (usually "ubuntu").
5. In "password" use the password that you use to log into lambda on the webiste.