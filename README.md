# Connecting Node.js Applications to Autonomous Transaction Processing

## Overview

Oracle Autonomous Transaction Processing delivers a self-driving, self-securing, self-repairing database service that can instantly scale to meet demands of mission critical applications. In this hands on lab, you will use Node.js to run an example application that connects to an Oracle Autonomous Transaction Processing database using the Oracle Instant client.

## Installing Node.js

For this hands on lab, Node.js version 12.9.1 for Microsoft Windows (x64) has already been installed. Node.js is available for several different operating systems and can be downloaded from https://nodejs.org/en/downloads. There are techniques for installing Node.js with administrative privileges such as root or administrator access, and techniques for installing without special privileges. The Microsoft Windows platform has an additional requirement to install the Visual Studio 2017 Redistributable. This step has already been performed.

## Installing Oracle Database driver for Node.js

**Using the Clipboard**

1. To copy content from the lab instructions to your OCI instance, select the content and use Ctrl-C to copy the content.

2. Click on the Clipboard icon and select **Paste to remote session**.

   <img src="https://raw.githubusercontent.com/oracle/learning-library/master/oci-library/qloudable/MachineLearning_ADW/img/ADW_CLIP.png" alt="Qloudable clipboard icon">

3. Click into the pop up window and press Ctrl-V.

4. Click in the tool or field where you want to paste and press Shift+Ins inside a Git-Bash window, or you can right-click inside the Git-Bash windows and select paste.

**Installing Oracle Database driver for Node.js**

1. Open a Git-Bash window.

   <img src="img/gitBash.png">

2. Navigate to the root folder of the C: drive.
```
cd /c
```

3. Create a new demo directory and change to that directory.
```
mkdir demo
cd demo
```

4. Verify that Node.js is installed.
``` 
node --version 
```

5. Determine the version of npm that is installed.
```
npm -v 
```

6. Use npm to install the Oracle Database driver for Node.js
``` 
npm install oracledb
```

7. Verify that the Oracle Database driver for Node.js has been installed.
```
npm list
```

## Install the Oracle Instant Client
For this hands on lab, the Oracle Instant Client for Microsoft Windows (x64) has already been downloaded and staged, but not installed. The Oracle Instant Client is typically downloaded from https://www.oracle.com/database/technologies/instant-client/downloads.html. It is currently stage in the **/c/OracleDB-Node.js-lab** folder.

1. Unzip the Oracle Instant into your **/c/demo** directory.
```
unzip /c/OracleDB-Node.js-lab/instantclient-basic-windows.x64-19.3.0.0.0dbru.zip
```

2. Change to the instantclient_19_3 subdirectory that was just created, and create network/admin subdirectories. The Oracle Wallet security credentials from the OCI database instance will need to be placed into the /c/demo/instanctclient_19_3/network/admin directory.
```
cd instantclient_19_3
mkdir -p 
```

3. Add the location of the installed Oracle Instant Client to the PATH variable persistently.
```
echo "export PATH=/c/demo/instanctclient_19_3:\$PATH" >> ~/.bashrc
source ~/.bashrc
```

## Sign in to the Oracle Cloud Infrastructure console

1. Launch the Chrome browser application (Same location that you launched Git-Bash). The home page should be set to the OCI sign in page.

2. Sign in to the OCI console using the following information.
* **Tenant Name:** {{Cloud Tenant}}
* **User Name:** {{User Name}}
* **Password:** {{Password}}
* **Compartment:** {{Compartment}}
* **Database Name:** {{Database Name}}
* **Database User:** admin
* **Database Password:** {{Database Password}}

3. Go to the service details page for your instance and select **DB Connection**

4. Select download and follow the on-screen instructions to create a password for this wallet. You will need this password in a later step.

5. Select download. The file is placed in the user's Downloads folder by the browser.

6. Change to the network/admin subdirectory for the Oracle Instant Client, and unzip the wallet. 
```
cd /c/demo/instanctclient_19_3/network/admin
unzip ~/Downloads/Wallet*.zip
```

## Install and Configure the Example Node.js Application 

1. Copy the example.js application to the **/c/demo** directory.
```
cp /c/OracleDB-Node.js-lab/example.js /c/demo
```

2. Edit the example.js application and set the username, password, and 
``` 
vi /c/demo/example.js
```
Make the following changes:
* Change the user to admin so it appears as follows: **user   : 'ADMIN'**
* Change the password to the password you created when downloading the wallet.
* Change the connectString to <database name>_low. Your connection string will be the name of your database followed by **_low**. Your database name is **{{Database Name}}**.
Example: If your database name was **Demo** then your connection string would be set as follows:  **connectString : 'demo_low'**

## Test your Node.js Application

Use the following commands to run your Node.js application:
```
cd /c/demo
node example.js
```

You should see the follwing output indicating success: ** [ [ 101, 'Alpha' ], [ 102, 'Beta' ], [ 103, 'Gamma' ] ].

The demo application 


## References

1. Youtube video of this hands on lab : https://www.youtube.com/embed/UG8z94vxYQE?rel=0&autoplay=1

2. Get Started and Provision an Autonomous Database : https://www.youtube.com/watch?v=Q6hxMaAPghI&autoplay=0&html5=1

3. Connecting with Python, node.js and other Scripting Languages : https://docs.oracle.com/en/cloud/paas/atp-cloud/atpug/connecting-nodejs.html#GUID-AB1E323A-65B9-47C4-840B-EC3453F3AD53

4. Oracle Instant Client : http://www.oracle.com/technetwork/database/database-technologies/instant-client/overview/index.html

5. Example.js Node Application : https://github.com/oracle/oracle-db-examples/blob/master/exadata-express/Example.js
