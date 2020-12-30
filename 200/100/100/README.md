# 100 Installing, Starting, and Shutting Down Nexus Repository

## Objectives
By the end this lesson, you will be able to:

- Download the latest version of NXRM.
- Unpack the archive and start the NXRM.
- Sign in and complete the setup wizard to update security defaults.
- Sign out and shut down the repository.

## Download Repository and Create Installation Directory
In order to practice using Nexus Repository Manager 3 in this lesson, you will need to create an installation directory. This is where you can download and store your instance of the repository manager. The installation directory will serve as the common parent location for all files needed to install and run NXRM.

Download the repository manager via these steps:

1. Create an installation directory on your computer.

- Tip: Best practice is to create your installation directory in a directory other than your user home directory and outside of the Program Files directory. You can install the repository manager in a directory other than your users home directory. On a Unix machine common practice is to use /opt. Navigate to the [Download page](https://help.sonatype.com/repomanager3/download/download-archives---repository-manager-3?_ga=2.162215228.1873063918.1609334621-230793279.1609334621) in our help documentation to access the latest version of Nexus Repository Manager. The latest version of the download file is displayed below. This example uses version 3.10.0-04.

2. Click the Link for Download according to your operating system. The packed/zipped file is downloaded to your computer.
3. You have now successfully created an installation directory and downloaded NXRM. Next, we will unpack the file and launch NXRM via the startup script.

Watch this [video](https://learn.sonatype.com/courses/nxrm-config-100/lessons/installing-starting-and-shutting-down-nexus-repository/) to see how to download the repository manager and create an install directory.

```
cd /opt
mkdir install_dir
```

## Unpack and Launch Repository Manager
After successfully downloading the NXRM file, unpack the compressed files into the file directory that you created in the section above. From that point, you will be able to launch the repository by running the startup script.

1. Unpack the archive file into the directory you created in the previous section. From the command line use ```tar xvzf nexus-<version>.<tar file extension>``` to extract the repository manager.
2. Locate the startup script for NXRM in the directory you created earlier in this lesson. You will find the startup script in the folder ```nexus-<version>/bin/``` as pictured above. (This example uses a Linux platform.)
3. Start NXRM by running the nexus file in your terminal. From the bin folder in your application directory perform one of the following:
- ```./nexus run```, for *Unix operating systems like Linux
- ```nexus.exe /run```, for Windows
4. Type in the URL http://localhost:8081/ in your browser. The Nexus Repository Manager Welcome screen displays.

The Welcome screen (aka Outreach page) provides important links and notifications regarding the repository manager. On this page you might find details about upcoming user conferences, release notes, and surveys, among other things. Navigating the user interface is covered in a separate module.

You have successfully unpacked and started NXRM 3 OSS. Up next, sign into the Repository Manager and complete the security wizard at startup.

Check out this [video](https://learn.sonatype.com/courses/nxrm-config-100/lessons/installing-starting-and-shutting-down-nexus-repository/) to learn to unpack and run Nexus Repository Manager.


## Signing In
The first time you log in to the repository manager, you’re required to create a new password. The initial password is an alpha-numeric string found in your data directory. The first attempt to get in takes you to a module to help you complete the steps, and to set up defaults for anonymous access.

Make sure your terminal is open to complete the authentication steps.


From the Welcome screen.
Click Sign in. A Sign in pop up box is displayed.
Navigate to …/sonatype-work/nexus3 in your terminal.
Locate the admin.password file.
Copy the string from the file to the password field, and sign in.
Click Next to start the Setup module.
Enter a new password then enter it again in the Confirm password field.
Click Next.
Decide whether you want to enable anonymous access or not in the Configure Anonymous Access modal.
Click Next.
Click Finish to complete the module.
Note
To see the progression of repository creation in this course, we recommend that you leave Enable Anonymous Access unchecked, as demonstrated in the video (Complete the Setup Module). Otherwise, if enabled, you will not be authorized to cache Java/Maven packages in your test proxy.
Change Your User Name and Profile
Update Your Account Profile
The first time you login to Nexus Repository, it is best practice to change the default credentials including your first and last name and email address. After logging in with your username and new password, from the previous section, complete the following steps:

From the Account screen.
Click Change password. The Authenticate dialog box is displayed.
Enter your First name, Last name, and Email in the appropriate open text fields.
Click Save. The screen refreshes and your account information is updated.

Change Your Default Password
If you ever need to change your password again, you can visit the Admin user profile account to do so.

From the Account screen.
Click Change password. The Authenticate dialog box is displayed. 
Enter your current password in the open text field.
Click Authenticate. The Change Password dialog box is displayed.
Enter a new password in the New password field.
Confirm the new password by entering it in again in the Confirm password field.
Click Change password. The dialog box is closed, and you have successfully changed your password.
You have now successfully logged in to NXRM and updated your account and passwords.

Check out this [video](https://learn.sonatype.com/courses/nxrm-config-100/lessons/installing-starting-and-shutting-down-nexus-repository/) to learn more signing in and updating credentials.


## Sign Out and Shut Down
In order to shut down the repository manager, there are a few things to do. First, sign out of NXRM, then shut down via the command line. The steps to do so are described below.

Click Sign out. The screen refreshes and you are signed out of NXRM. You may close the browser window.
Navigate to your terminal.
You can do a hard stop with CTL+C on the keyboard.
Alternatively, you can run nohup ./nexus stop to shut down the application. nohup produces a log file – nohup.out – that records the status of your Nexus instance.

Watch this [video](https://learn.sonatype.com/courses/nxrm-config-100/lessons/installing-starting-and-shutting-down-nexus-repository/) to see how to sign out and shut down Nexus Repository.
