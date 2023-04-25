# Server Networking Lab

## Task

In this lab, we are going to practice connecting our host computer to our VM server via `ssh`. In addition, we will transfer some files between both systems using `FTP`. Make sure FileZilla is already installed on your computer!

## Instructions

### Connecting to your VM

In your virtual machine, run the following command:

```bash
$ ifconfig
```

Once again take note of the IP address marked as `inet`. This is the IP address we will use to `ssh` into the VM.

On your host machine, open a terminal of your choice and run the following command, replacing the user and IP with your VM user and address:

```bash
$ ssh <user>@<vm_ip>
```

When prompted to enter a password, use your VM user's password. Once logged in, you should see some system information output. Take a screenshot of this output for submission. 

Now you can run commands on your VM from your host PC as if you were using the actual VM. A real use-case is if you have a remote server that's *not* on your PC, for example using a service like *Amazon AWS*, and you want to run commands on that machine from your location.

Once finished, you can type "quit" to close out the SSH connection.

### Transferring a file using FileZilla

To begin, create a text file on your host machine called `ftp_file.txt` and fill it with any text you like. Alternatively, you may run the following command in a directory that you have easy access to:

```bash
$ echo "This file will be created on my system, then be transferred into my virtual machine using FileZilla using the FTP protocol." > ftp_file.txt
```

Next, open FileZilla. Click "Site Manager" in the top left corner. When this menu opens, you should see your VM from the prior lessons listed in the "My Sites" tree on the left hand side. Verify that the IP address listed for your VM is the same as the IP address we used to SSH. In addition, confirm that the credential fields are filled out correctly, i.e. Login Type of "Normal", user and password. 

Once done, hit "Ok" and you should see a connection to "Local site" and "Remote site", each displaying a file tree. On the left, traverse through your directories until you find the `ftp_file.txt` file we just created. Then, on the right make sure you are in your `home/<user>` directory.

Click and drag your `ftp_file.txt` from the left to the right inside the `<user>` folder.

### Ensure File Transfer was Successful

To confirm that our FTP succeeded, find the "Successful transfers" tab at the bottom of FileZilla. Click into this tab and you should see our most recent transfer listed. Take a screenshot of FileZilla with this tab open for lab submission.

## Submission

Submit the screenshots of terminal output for the SSH session, as well as the screenshot with your successful FileZilla FTP results.

