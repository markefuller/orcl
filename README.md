# Connecting Node.js Applications to Autonomous Transaction Processing

## Overview

Oracle Autonomous Transaction Processing delivers a self-driving, self-securing, self-repairing database service that can instantly scale to meet demands of mission critical applications. In this hands on lab, you will install Node.js and use a small example application to connect to an Oracle Autonomous Transaction Processing database using the Oracle Instant client.

## Installing Node.js

For this hands on lab, Node.js version 12.9.1 for Microsoft Windows (x64) has already been installed. Node.js is available for several different operating systems and can be downloaded from https://nodejs.org/en/downloads. There are techniques for installing Node.js with administrative privileges such as root or administrator access, and techniques for installing without special privileges. The Microsoft Windows platform has an additional requirement to install the Visual Studio 2017 Redistributable. This step has already been performed.

## Installing Oracle Database driver for Node.js
1. Verify the version of Node.js installed.
``` Node --version ```

## Sign in to OCI Console

* **Tenant Name:** {{Cloud Tenant}}
* **User Name:** {{User Name}}
* **Password:** {{Password}}
* **Compartment:** {{Compartment}}
* **Database Name:** {{Database Name}}
* **Database User:** admin
* **Database Password:** {{Database Password}}


Sign in using your tenant name, user name and password. Use the login option under **Oracle Cloud Infrastructure**

**Using the Clipboard**

1. To copy content from the lab instructions to your OCI instance, select the content and use Ctrl-C to copy the content.

2. Click on the Clipboard icon and select **Paste to remote session**.

   <img src="https://raw.githubusercontent.com/oracle/learning-library/master/oci-library/qloudable/MachineLearning_ADW/img/ADW_CLIP.png" alt="Qloudable clipboard icon">

3. Click into the pop up window and press Ctrl-V.

4. Click in the tool or field where you want to paste and press Ctrl-V again.

## References

1. Youtube video of this hands on lab : https://www.youtube.com/embed/UG8z94vxYQE?rel=0&autoplay=1

2. Get Started and Provision an Autonomous Database : https://www.youtube.com/watch?v=Q6hxMaAPghI&autoplay=0&html5=1

3. Connecting with Python, node.js and other Scripting Languages : https://docs.oracle.com/en/cloud/paas/atp-cloud/atpug/connecting-nodejs.html#GUID-AB1E323A-65B9-47C4-840B-EC3453F3AD53

4. Oracle Instant Client : http://www.oracle.com/technetwork/database/database-technologies/instant-client/overview/index.html
