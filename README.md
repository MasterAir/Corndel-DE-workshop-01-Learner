# Data Engineer Workshop 1: Setting up your Data Engineering workspace and tools

Our first Data Engineer workshop builds upon the last exercise at your launch event where you explored what you can do with your A Cloud Guru (ACG) account. Remember, you created cloud sandboxes for Azure, AWS and Google Cloud Platform (GCP): https://learn.acloud.guru/cloud-playground/cloud-sandboxes and also created and logged in to a Window Virtual Machine (VM) using the Windows Remote Desktop Connection app: https://learn.acloud.guru/cloud-playground/cloud-servers

At this first workshop, we will build on that first exploration so you can learn how to use both the Windows VM and cloud sandboxes to take part in workshops. We will also do a simple data exercise at the end.

This is a supportive technical onboarding workshop that also gets you familiar with the interactive style of workshops we will have together going forward. 

**Before you attend the workshop, please make sure you have done the following described in the next section.**

## Before the workshop please ensure you have: 

1. **Tools installed on a work laptop:** Ideally, have a work laptop with VS Code, Git, Python, Azure Data Studio and Windows Remote Desktop Connection app installed that can connect to an ACG Windows VM. Or, at the very least, a work laptop with the Windows Remote Desktop Connection app installed that can connect to an A Cloud Guru (ACG) Windows Virtual Machine.
2. **Aptem:** Completed the first two e-learning modules in Unit 1 and their subsequent Data Engineer Pass Descriptor questions:
    - **1.1 The Uses of Cloud Computing Platforms:** De-mystifies what cloud and on-premises are. You are then tasked in Aptem to describe briefly your own organisation's use of the cloud to support you in evidencing a Data Engineer Pass descriptor in Aptem. 
    - **1.2 Data Engineering in Your Organisation:** Supports you in describing your own organisation's data architectures and their relevant data development frameworks, data engineering tools used, and end data use cases across organisations. You are then tasked in Aptem to describe these three topics to evidence several Data Engineer Pass descriptors.

## Key

> 💻 - Activity for you to do <br>
 ❓ - A question for you and your group <br>
ℹ Important note (e.g. data security reminder) <br>
↩ After clicking a footnote in the text, use this arrow to return <br>
🎉 - Well done, completing the activities up to this point is all you need to do in the workshop. If time allows, stretch yourself further with the rocker activities described next<br>
🚀 - A going further stretch activity only if your time allows <br>

> ℹ️ Open any web links by right-clicking and selecting `Open link in new tab` so that this page remains visible

<a id="contents"></a>

## Contents

- [Learning Outcomes](#outcomes)
- [Data Engineer Pass Descriptors Targeted](#descriptors)
- [MORNING - Set up your data engineering Windows Desktop](#morning)
  - [💻1️⃣ Create Windows Virtual Machine and connect (~20 mins)](#vm)
  - [💻2️⃣ Install VS Code (~15 mins)](#vs)
  - [💻3️⃣ Install Python (~15 mins)](#python)
  - [💻4️⃣ Install Git (~15 mins)](#git)
  - [🚀5️⃣ Set Git credentials (~10m)](#git-creds)
  - [🚀6️⃣ Create and connect to a Linux Virtual Machine (~45 mins)](#Linux)
  - [🚀7️⃣ Install and test Docker in Linux Virtual Machine (~30 mins)](#docker)
- [AFTERNOON - Using Cloud Sandboxes](#afternoon)
  - [💻8️⃣ Start cloud sandbox (Azure) and deploy a simple SQL data architecture (~10 mins)](#azure)
  - [💻9️⃣ Setup a windows server VM in your Azure sandbox](#azureVM)
  - [💻1️⃣0️⃣ Query your database with MS recommended tools (~20 mins +)](#tools)
  - [🚀1️⃣1️⃣ Get to know your data with simple SQL (~60m +)](#know)
- [Preparation for next workshop](#next)

<a id="outcomes"></a>

## Learning Outcomes

[Back to Contents](#contents)

1. **Understanding Virtual Machines:** Practical experience setting up and managing cloud-based virtual machines (VMs) in Azure and so start to understand key concepts of Infrastructure as a Service (IaaS).
2. **Development Environment Configuration:** Learn to configure and use key data engineering tools such as Visual Studio Code, Python, and Git on a cloud-based VM, highlighting the integration of these tools in a typical data engineering workflow.
3. **Version Control:** Start to experience using Git for version control.
4. **SQL and Database Management Skills:** Develop foundational skills in SQL through the creation and querying of a database in Azure SQL.
5. **Querying a database with a SQL tool:** Experiment with a SQL data querying tool recommended by Microsoft.

<a id="descriptors"></a>

## Data Engineer Pass Descriptors Targeted today

[Back to Contents](#contents)

As described at the launch event, at the end of the Data Engineer programme you will be independently assessed against 35 Data Engineer "Pass Descriptors" through a **supportive** discussion. They succinctly describe what you will need to evidence. Take a quick look now at the 35 Data Engineer pass descriptors now <https://www.instituteforapprenticeships.org/apprenticeship-standards/data-engineer-v1-0?view=standard#grading>

Your workshops, including this one, aim to let you practically experience most of the topics in the pass descriptors so that your learning is not only theoretical but also hands-on. Practical learning improves your ability to meet the pass descriptors effectively through the real data engineering project in your organisation, any wider data engineering tasks you carry out and from your growing knowledge of data engineering inside and outside your organisation.

This launch workshop will already start to support you in understanding and developing yourself towards several of the 35 pass descriptors. In particular, this workshop targets these four pass descriptors:

> Outlines the uses of **different on-demand cloud computing platforms**. (K14)

> Software development principles for data products, including debugging, **version control**, and testing. (K6)

> Explains how they have **worked with different types of data stores** to monitor and optimise the performance of data products. (K1, S7)

> Demonstrates the use of tools and programming to **query and manipulate data** and implement automated validation checks, showing the methodologies used for moving data from one system to another for storage and handling. (K2, S9)

We will do this when you use the A Cloud Guru (ACG) platform and start to use **different public on-demand cloud computing platforms**. You will be setting up Git, that allows **version control**, and through the creation of a SQL database **data store** you will begin to **query and manipulate data** with SQL.

Don't worry if any of these phrases or tools are new to you all instructions are provided below and we will come back to all these concepts, tools and techniques throughout the programme.

<a id="morning"></a>

## MORNING - Set up your data engineering Windows Desktop

[Back to Contents](#contents)

Our session this morning is about ensuring you have a computer that let's you fully take part in all of the Data Engineer workshops throughout the programme. In summary, the aim is for you to have a computer with VS Code, Python, Git and Azure Data Studio installed that you have tested and are working.

One option to take part in our workshops is to use ACG to create a Virtual Machine (VM)ℹ and access it remotely using Windows Remote Desktop[^1]. The Virtual Machine you create is simply a computer in the cloud, much like a desktop computer but typically more powerful. A VM is an example of *Infrastructure as a Service (IaaS)*[^2] in an on-demand cloud computing platform that you learned about in your first e-learning module.

> ℹ Virtual Machines in ACG should only be used with non-sensitive public data and **not** include any of your organisation's data. You will have read and signed a document already acknowledging you have read and understood your appropriate use of ACG services.

Even if you have a laptop with the software needed, the activities this morning are still useful hands-on exercises for a data engineer to become familiar with VMs and the installation of key software tools.

Having set up your data engineering desktop in the morning, in the afternoon, we will carry out a short data exercise that will be very similar in style to many later workshops that use the cloud.

**Summary:** Our ultimate goal today is summarised in the animation below. To set yourself up so that, from a work laptop, you have all the tools you need to take part in workshops, potentially through a Virtual Machine, and then go to create and query a database in the cloud using SQL.

| ![Summary](/images/ws_overview.gif) |
|:--:|

[^1]: Guide to using Windows Remote Desktop: <https://support.microsoft.com/en-us/windows/how-to-use-remote-desktop-5fe128d5-8fb1-7a23-3b8a-41e636865e8c#ID0EDD=Windows_1>

[^2]: Good explanation of Infrastructure as a Service (IaaS) is: <https://cloud.google.com/learn/what-is-iaas>

## 💻 Breakout room guidelines

1. Keep your camera on in the breakout room.
2. Introduce yourself to anyone in the room you have not met before.
3. Start each exercise by discussing any questions marked with "❓".
4. For each activity, one person can screen share and everyone else can follow along. Then, switch to someone else screen sharing to complete the next activity.
5. Share your progress and ask for help when needed.
6. Embrace a growth mindset and understand that it's normal to not know everything. 
7. Use online resources and chatbots, or ask for help from your peers and PDE as you go along.
8. Be a good breakout room participant by contributing and staying positive.
9. Encourage everyone's participation.
10. Respect others' opinions and viewpoints.


<a id="vm"></a>

### 💻1️⃣ Create Windows Virtual Machine and connect (~20 mins)

[Back to Contents](#contents)

> ❓ In your group, discuss and compare what your company has provided to you to take part in the apprenticeship. Perhaps VS Code, Git, Python and Azure Data Studio are installed for you onto your work laptop, or  you have a laptop with install rights, or perhaps you will need to use a Windows Virtual Machine you are about to create together?

1. Go to A Cloud Guru (ACG) `Cloud Servers`[^3] page and login: <https://learn.acloud.guru/cloud-playground/cloud-servers>

2. Click `+ New Server` blue button, then
    - For `Distribution` select `Windows Server 2022`
    - For `Zone` select the closest to you (perhaps `Europe`)
    - For `Size` select `Large`
    - (`Tag` is not important unless you had a large number of virtual machines with the same use and you wanted to easily identify them)

3. When your VM shows it is `Ready`
    - Open Windows Remote Desktop Connection (in the search box of your windows task bar each for `remote`),
    - Click `Show options`, then
    - Copy and paste the ACG public IP address from the `Public IP4` box into the `Computer` box of the Remote Desktop dialog (shown below).

| ![Connect to VM](/images/cloudserver.png) |
|:--:|

> ℹ Your VM will shut down automatically after 4 hours, saving everything in the VM. If the VM remains shut down for 14 days, everything in the VM will be deleted. So, if you want to keep everything in your VM, you should restart the VM before the 14-day deletion deadline. However, if it is deleted, do not worry; you have these workshop instructions for how to quickly re-install the tools needed for the workshops.

| ![Shut down of VM](/images/autoshutdown.png) |
|:--:|

[^3]: ACG guide to Cloud Servers: <https://help.pluralsight.com/help/cloud-servers>

<a id="vs"></a>

### 💻2️⃣ Install VS Code (~15 mins)

[Back to Contents](#contents)

VS Code is a powerful code editing development environment known as an IDE (Integrated Development Environment).

> ❓ In your group, discuss any previous experience with VS Code and what you have used it for. Or, perhaps you use other IDEs for coding, such as PyCharm? What do you like and not like about VS Code, Pycharm or any other IDE for coding?

In your Windows VM, you can install VS code manually from here: <https://code.visualstudio.com/download>

Or... consider following the instructions below to use a PowerShell script[^4] that automates the installation of VS Code and useful extensions[^5].

1. In your Windows VM, open Powershell[^6] as administrator. You can do this by:
    - 1️⃣ Searching for  `Powershell` in the search box of the taskbar,
    - 2️⃣ Then right click on `Windows PowerShell` and
    - 3️⃣ Select `Run as administrator`.

| ![powershell](/images/powershell.png) |
|:--:|

2. Install Nuget[^7]

```bash
Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force
```

3. At the Powershell prompt, copy and paste the PowerShell commands below one after the other. They will save a PowerShell script to your Downloads folder.

```powershell
cd 'C:\Users\cloud_user\Downloads'
```

```powershell
Find-Script -Name Install-VSCode -Repository PSGallery | Save-Script -Path .
```

4. At the Powershell prompt, copy and paste the Powershell command below that will find the install script for  VS Code you just downloaded, then use that script to install VS Code with additional useful extensions.

```powershell
.\Install-VSCode.ps1 -LaunchWhenDone -AdditionalExtensions 'ms-mssql.sql-database-projects-vscode', 'ms-mssql.mssql', 'ms-azuretools.vscode-docker', 'github.vscode-pull-request-github', 'eamodio.gitlens', 'aykutsarac.jsoncrack-vscode', 'ms-toolsai.jupyter', 'ms-python.python', 'donjayamanne.python-extension-pack', 'mechatroner.rainbow-csv', 'ms-vscode-remote.remote-ssh', 'ms-vscode.remote-explorer', 'tomoki1207.pdf', 'ms-python.black-formatter', 'ms-python.flake8'
```

[^4]: VS Code install PowerShell script used in this exercise: <https://www.powershellgallery.com/packages/Install-VSCode/1.4.3>

[^5]: VS Code Extensions marketplace: <https://code.visualstudio.com/docs/editor/extension-marketplace>

[^6]: PowerShell is a versatile command line tool for task automation and system management in Windows from simple administrative tasks to complex scripting. For an in-depth understanding, visit Microsoft's guide: <https://learn.microsoft.com/en-us/training/modules/introduction-to-powershell/>

[^7]: NuGet is a package manager for the Microsoft development platform, including .NET. It's essential for managing the installation of various software packages and dependencies in the .NET framework: <https://docs.microsoft.com/en-us/nuget/what-is-nuget>

<a id="python"></a>

### 💻3️⃣ Install Python (~15 mins)

[Back to Contents](#contents)

In later workshops, we will build data pipelines using Python. Let's install Python and test that we can use it from a Jupyter notebook in VS Code.

> ❓ In your group, discuss any previous experience with using Python. What do you like about Python? What do you find challenging? Do you have any learning goals for Python?

1. From this link, download the latest version of Python for Windows: <https://www.python.org/downloads/>

2. Using Windows Explorer, find the downloaded file, and right-click on it and select `Run as administrator...` to install Python.

3. If you used the Powershell script method above to install VS Code, you will have the Python[^8] and Jupyter[^9] VS Code extensions already installed. If you installed VS Code by downloading its install file, you can add the extensions manually as follows:
    - 1️⃣ Click on the Extensions view icon on the Sidebar (or press Ctrl+Shift+X) to open the Extensions view.
    - 2️⃣ In the Extensions view search bar, type `Python`. Locate the Python extension by Microsoft (it should be the first result, as shown below).
    - 3️⃣ Click the blue `Install` button. Once clicked, the installation will start.
    - 🔁 Now repeat the steps above but this time search for `Jupyter`.<br>

| ![extension](/images/vscode-extensions.png) |
|:--:|

4. From the VS Code main menu, select `File / New File...` then `Jupyter notebook` to open a blank Jupyter notebook.

5. Now do the following to test you can run Python code: <br>
    1️⃣ In the right-hand corner of the notebook, check that Python is selected.<br>
    2️⃣ Copy and paste the Python code below into the first cell of the notebook and run that cell using the play button next to it. When you click the play button to run the cell, you are likely to be prompted to install the required `ipykernel` package. Accept this suggestion.<br>

```python
import sys
print(sys.version)
```

| ![python](/images/python.png) |
|:--:|

6. In later workshops, we will install Python packages directly into this Python environment and into something called virtual Python environments. In order to be able to install new Python packages, we need to edit a Windows environment variable called Path that will tell the operating system where to find the Python executable and associated scripts so that Python commands and packages can be executed without specifying the full path. In the Search box in the Windows taskbar search for environment and select `Edit the system environment variables` then: <br>
    1️⃣ As shown below, click on the `Environment Variables` button to open the next dialog. <br>
    2️⃣ Select the `Path` environment variable. <br>
    3️⃣ Click the `Edit` button to open the next dialog. <br>
    4️⃣ Click the `New` button and add the following paths. Before you add them, check that exact folder exists using Windows Explorer; the last folder name will be different with different versions of Python:<br>`C:\Users\cloud_user\AppData\Local\Programs\Python\Python312` <br>
    Click the `New` button again and add the following path as well: <br>`C:\Users\cloud_user\AppData\Local\Programs\Python\Python312\Scripts` <br>
  
| ![Clone](/images/path.png) |
|:--:|



[^8]: The Python VS Code extension: <https://marketplace.visualstudio.com/items?itemName=ms-python.python>
[^9]: The Jupyter VS Code extension: <https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter>

<a id="git"></a>

### 💻4️⃣ Install Git (~15 mins)

[Back to Contents](#contents)

Let's install Git software. Git is a powerful version control system widely used in software development, including data engineering, for tracking changes in code and collaborating with others.

In later workshops, having Git will allow you to easily copy the workshop files to your own computer (called "cloning"[^10]). Using GitHub allows version control, which is a software development best practice described in one of the Data Engineer pass descriptors. We will cover software development best practices in later modules and workshops.

If you are new to Git and GitHub, we recommend several good resources provided by GitHub to self-tailor your learning[^11].

> ❓ In your group, discuss any previous experience with using Git, GitHub, and version control in general. What do you like about using Git/Github and what do you find challenging? What are your learning goals with Git/GitHub?

1. Download and install[^12] the latest version of Git from here: <https://git-scm.com/downloads>

Next, if you don't yet have a GitHub account yet, create one by following these instructions: <https://docs.github.com/en/get-started/quickstart/creating-an-account-on-github>

Now that you have a Windows Virtual Machine desktop with VS Code, Python and Git installed, let's "clone" the repository for this workshop. While cloning the workshop material is not essential to take part in the workshops, this is a valuable skill to develop as a data engineer.

2. Open VS code and click on  `Clone Repository`, then `Clone from GitHub` at the top.

| ![Clone](/images/clone.png) |
|:--:|

3. Click `Allow` and sign in to GitHub in the browser that opens.

| ![Allow github access](/images/allow.png) |
|:--:|

4. You should now be able to repeat step 2 above, but when you click on `Clone from GitHub` at the top, it will give you a list of repositories you can clone. Also, try copying and pasting the URL for this repository into the window at the top after selecting 'Clone from GitHub'. Then, select where you will store the files on your computer.

| ![Clone](/images/clone.png) |
|:--:|

[^10]: Cloning means creating an exact replica of a repository, similar to downloading a music playlist onto your device. Just as you get a personal copy of the music to enjoy and use independently, cloning gives you your own version of the code to work on and modify without affecting the original: <https://github.com/git-guides/git-clone>

[^11]: This short tutorial is a practical hands-on way to become familiar with the main concepts in Git: <https://docs.github.com/en/get-started/quickstart/hello-world> While the Git Guide is a good way to read about Git and understand it well conceptually: <https://github.com/git-guides>. Further, if you wanted to go from zero to the most advanced skills and topics in GitHub, the GitHub SKills page is a great one-stop resource: <https://skills.github.com/>

[^12]: Setting up Git guidance: <https://docs.github.com/en/get-started/quickstart/set-up-git#setting-up-git>

## 🎉 If you have completed all the 💻 activities up to this point, congratulations! If time allows before the lunch break, continue with the 🚀 going further activities below.

<a id="git-creds"></a>

### 🚀5️⃣ Set Git credentials (~10 mins)

[Back to Contents](#contents)

As well as being able to clone repositories of code in GitHub, to be able to contribute to repositories, you will also need to set your Git commit username[^13] and commit email address for Git[^14]. The short exercise below takes you through how to enable that.

Being able to contribute to GitHub repositories through commits[^15] is not necessary to take part in the workshops, but it is a very useful skill to develop as a data engineer.

[^13]: How to set your Git username: <https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git#setting-your-git-username-for-every-repository-on-your-computer>

[^14]: How set your commit email address in Git: <https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address#setting-your-commit-email-address-in-git>

[^15]: Explanation of Git commit: <https://github.com/git-guides/git-commit>

<details><summary>If time allows</summary>

You can set your Git username and email in VS Code by following these instructions: <https://learn.microsoft.com/en-us/visualstudio/version-control/git-settings?view=vs-2022#name-and-email>

Or using the terminal as follows:

1. Open a new terminal in VS Code from the menus `Terminal / New Terminal` or the keyboard shortcut `Ctr+Shift+'`

2. Once the terminal is open, enter the following commands in the terminal, replacing `<your-github-username>` and `<your-github-email>` with a username and the email address in your GitHub account. The username name doesn't need to match your GitHub username.

To set your GitHub username, use:

```bash
git config --global user.name "<your-github-username>"
```

To set your GitHub email, use:

```bash
git config --global user.email "<your-github-email>" 
```

</details>

<a id="Linux"></a>

### 🚀6️⃣ Create and connect to a Linux Virtual Machine (~ 45mins)

[Back to Contents](#contents)

In this exercise, you'll learn how to create and connect to a Linux Virtual Machine (VM) from a Windows VM using a remote connection in Visual Studio Code (VS Code). While Linux is not required for the workshops, nor is it described in the Data Engineer pass descriptors, practical hands-on experience with connecting to and using Linux remotely in multiple ways is highly beneficial for data engineers giving you cross-platform skills between Windows and Linux, often needed in data engineering environments.

As time allows, follow the steps below to set up and remotely access a Linux VM from VS Code on Windows.

> ❓ If your group has time, discuss any experience you have with Linux. Do you use it in your organisation? Do you prefer Linux to Windows? What do you find easy or difficult to do with Linux compared to Windows? Do you have any Linux learning goals?

![remote development](https://code.visualstudio.com/assets/docs/remote/ssh/architecture-ssh.png)

> Image from: <https://code.visualstudio.com/docs/remote/remote-overview>

<details><summary>If time allows.</summary>

1. Go to this ACG cloud servers link and create a Linux VM by selecting the `Ubuntu 22.04 - Jammy Jellyfish`: <https://learn.acloud.guru/cloud-playground/cloud-servers>

2. Use the `Open Terminal` button and log in to your new Linux VM with the username `cloud_user` and use the temporary password provided. Then, when prompted, change the default password.

| ![terminal](/images/openterminal.png) |
|:--:|

3. Now go back to your Windows VM you connected to with Windows Remote Desktop, open VS Code and install the VS Code extension `Remote - SSH` extension. Do this as follows:

- Go to the Extensions view (`Ctrl+Shift+X`).
- Search for `Remote - SSH` and install the extension provided by Microsoft (if not already installed)

4. You can now connect remotely from VS Code in Windows to your remote Linux VM. However, you would need to enter your Linux password each time. Instead, let's set up SSH keys for a passwordless login. This involves generating a pair of cryptographic keys on your local Windows VM and then adding the public keyℹ️ to this file in your Linux VM directory here `~/.ssh/authorized_keys` To generate an SSH key pair on your Windows machine, open a terminal and enter...

```bash
ssh-keygen
```

When prompted to enter a filename and then a passphrase you can leave both blank and just hit your return key.

> ℹ️ The public key `id_rsa.pub`` can be shared freely but the private key`id_rsa` (with no file extension) should never be shared.

5. Connect to Your Linux VM

- Open the Command Palette in VS Code (`Ctrl+Shift+P`) or `F1`.
- Start typing this and select it: `Remote-SSH: Connect to Host...` then hit the return key.
- Enter the SSH connection command: `cloud_user@vm-ip-address` where the vm-ip-address will be the public IP of the Linux VM you recently created and can be found here: <https://learn.acloud.guru/cloud-playground/cloud-servers>
- Select `Linux` from the three options that appear.
- Click `Continue` when prompted and enter the password of your Linux VM you recently changed when prompted.

6. Once connected, you can open folders, edit files, and run commands as if you were working locally on the Linux VM! You can continue to work this way but you'll need to keep entering your Linux VM password. To avoid entering your password each time, let's now copy the public key we created earlier in your Windows VM into the right part of your Linux VM.

- Using VS Code explorer view navigate to the `.ssh` directory and open the `authorized_keys` file.
- Or, you can access the same file by opening a terminal in VS Code, navigate to the same folder, view its contents and open the  `authorized_keys` by entering these commands:

```bash
cd .ssh
```

```bash
code authorized_keys
```

7. Now in Windows Explorer of your Windows VM, go to the folder `C:\Users\cloud_user\.ssh` and open the file `id_rsa.pub` in Notepad. Copy the text you see and paste it at the end of the `authorized_keys` file you have just opened in the remotely connected VS Code, then save the file. You should now find when you remote connect from your Windows VS Code to the Linux VM you do not need to enter the password of the Linux VM!

8. Now that you have remote connected to your Linux VM from your Windows VS Code, you could try a quick data file exploration exercise to start to become familiar with Linux/Unix commands[^16].

- Download a small csv file

```bash
wget https://raw.githubusercontent.com/MicrosoftLearning/dp-203-azure-data-engineer/master/Allfiles/labs/11/data/2019.csv
```

- Check the file size

```bash
ls 2019.csv -lh 
```

- Use head to display the first few lines of the file.

```bash
head 2019.csv
```

- search for rows that contain the text "Prasad"

```bash
grep -iwn "Prasad" 2019.csv
```

- we have used three options for our text search command of `grep`, of `i`, `w` and `n`. Run the following to understand what all those options provide.

```bash
grep --help
```

[^16]: Good guide to Linux/Unix commands <https://www.geeksforgeeks.org/essential-linuxunix-commands/> and  consider the overall Linux tutorial <https://www.geeksforgeeks.org/linux-tutorial/> for a comprehensive coverage of Linux.

</details>

<a id="docker"></a>

### 🚀7️⃣ Install and test Docker in Linux Virtual Machine (~30 mins)

[Back to Contents](#contents)

While Docker[^17] is unlikely to be used in our workshops, we include how to install and use Docker in your Linux VMℹ️ as a going further exercise. This is a valuable skill as a data engineer that may also be relevant to your organisation.

> ❓ If your group has time, discuss any experience you have with Docker. Do you you use it in your organisation? What do you find easy or difficult to do with Docker? Do you have any learning goals for Docker or equivalent services on the cloud, such as AWS Elastic Container Service (ECS), or Azure Container Instances?

> ℹ️ For simplicity, we would ideally install Docker Desktop on your Windows VM. However, this is not possible as nested virtualisation is not enabled and is generally not recommended by Docker: <https://docs.docker.com/desktop/vm-vdi/>

[^17]: What is Docker? <https://docker-curriculum.com/#what-is-docker->

<details><summary>If time allows.</summary>

1. In your Linux VM, follow the Docker Ubuntu instructions here to install Docker <https://docs.docker.com/engine/install/ubuntu/> then restart your Linux instance with:

```bash
reboot
```

2. To test your installation of Docker is working run the following command in your terminal. This command instructs Docker to run the pgAdmin docker container[^18] we can then use it connect to a postgresSQL database (which might also be in a docker container or hosted in the cloud). The -p 8082:80 option maps port 80 of the container to port 8082 on your VM, allowing you to access the pgAdmin interface through your browser at <http://localhost:8082>. The environment variables -e PGADMIN_DEFAULT_EMAIL and -e PGADMIN_DEFAULT_PASSWORD are used to set the default login credentials for pgAdmin.

```bash
docker run -p 8082:80 --name pgadmin4 -e PGADMIN_DEFAULT_EMAIL=myemail@example.com -e PGADMIN_DEFAULT_PASSWORD=mypassword -d dpage/pgadmin4
```

3. Then open pgadmin at this link in your Windows VM: <http://localhost:8082/>

[^18]: PgAdmin docker container guidance: <https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html>

</details>

<a id="afternoon"></a>

## AFTERNOON - Using Cloud Sandboxes

[Back to Contents](#contents)

Welcome back from your lunch break. So far this morning you have set up a virtual Windows Virtual Machine (VM) with most of the tools we need to take part in the workshops.

While not needed to take part in the workshops, you may also have completed the going further 🚀 exercises, for example, to create and connect to a Linux VM  is a valuable skill in many data engineering roles.

This afternoon, our main activity is to create and use an Azure "Sandbox" for a data exercise that will be similar in style to many of our later workshops where the cloud is used.

A sandboxℹ means a safe play area where we can experiment without incurring any costs. Each cloud sandbox is simply a temporary cloud account in Azure, AWS, or Google Cloud Platform, where most[^19] of its services are available for us to experiment with and learn practically with hands-on exercises. You do not need to worry about any costs incurred or deleting any services you create.

> ℹ The cloud sandboxes we create should only be used with non-sensitive public data and **not** include any of your organisation's data. You will have read and signed a document already acknowledging you have read and understood your appropriate use of ACG services.

[^19]: If a service is not available it will simply not create. Sometimes whole service are blocked that can lead to lots of expensive compute activities (e.g. Azure Databricks and Azure HDInsight), or particular configurations of services that can become expensive (e.g. a database with a lot of storage or compute): <https://help.pluralsight.com/help/cloud-playground>

<a id="azure"></a>

### 💻8️⃣ Start cloud sandbox (Azure) and deploy a simple SQL data architecture (~ 20 mins)

[Back to Contents](#contents)

Let's now set up an Azure Cloud sandbox, complete with a sample database. We'll then query this data using straightforward SQL commands.

These steps echo what we'll explore in our forthcoming SQL workshops, where we use a script to establish the necessary SQL data environment.

Below are the steps to create a basic data architectureℹ️ of a SQL server and a database housed on this server, including sample data. The script also configures firewall rules so that the database can be accessed over the internet from any IP address.

> ℹ️ This process is an example of what's known as **P**latform **a**s **a** **S**ervice (PaaS), a concept that was explained in your first e-learning module. Additionally, in your second module, we looked at the concept of data architecture.

| ![ARM-template](/images/ARM-template.png) |
|:--:|

> ❓ Discuss in your group any prior experience you have using Azure, AWS, GCP or any other cloud platform. Do you have a preference for one cloud provider over the other? Is there a particular cloud provider you would like to develop yourself further in that would benefit your organisation?

1. To create and connect to an Azure sandbox, start by right-clicking on this link to open in a new tab: <https://learn.acloud.guru/cloud-playground/cloud-sandboxes>, then click on the blue `Start Azure Sandbox` button. You should then see the screen below:

| ![azure](/images/azure.png) |
|:--:|

2. As shown in the above screen of your Azure sandbox details:
    - 1️⃣ Right-click on the blue `Open Sandbox` button  and select to open in a `private` or `incognito` window. This is so that your sandbox login does not conflict with an existing cloud account you may be using already.
    - 2️⃣ Then, copy and paste the  `Username` into the Azure login page in that private/incognito window.
    - 3️⃣ Then, copy and paste the `Password` into Azure login page in that private/incognito window.

3. Once you have logged in to your Azure sandbox, in the search box, type `arm` and select `Deploy a custom template` shown below in the red box.

| ![azure](/images/ARM.png) |
|:--:|

4. In the screen that appears, select `Build your own template in the editor` and copy and paste the json code below entirely over the default text showing. Then click `Save`.

```json
{
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "serverName": {
            "defaultValue": "[uniqueString('sql', resourceGroup().id)]",
            "type": "String"
        },
        "sqlDBName": {
            "defaultValue": "AdventureWorksLT",
            "type": "String"
        },
        "location": {
            "defaultValue": "[resourceGroup().location]",
            "type": "String"
        },
        "administratorLogin": {
            "type": "String"
        },
        "administratorLoginPassword": {
            "type": "SecureString"
        },
        "maxSizeBytes": {
            "defaultValue": 2147483648,
            "type": "Int"
        }
    },
    "resources": [
        {
            "type": "Microsoft.Sql/servers",
            "apiVersion": "2019-06-01-preview",
            "name": "[parameters('serverName')]",
            "location": "[parameters('location')]",
            "properties": {
                "administratorLogin": "[parameters('administratorLogin')]",
                "administratorLoginPassword": "[parameters('administratorLoginPassword')]",
                "publicNetworkAccess": "Enabled"
            }
        },
        {
            "type": "Microsoft.Sql/servers/databases",
            "apiVersion": "2020-08-01-preview",
            "name": "[format('{0}/{1}', parameters('serverName'), parameters('sqlDBName'))]",
            "location": "[parameters('location')]",
            "dependsOn": [
                "[resourceId('Microsoft.Sql/servers', parameters('serverName'))]"
            ],
            "sku": {
                "name": "Basic",
                "tier": "Basic"
            },
            "properties": {
                "maxSizeBytes": "[parameters('maxSizeBytes')]",
                "sampleName": "AdventureWorksLT"
            }
        },
        {
            "type": "Microsoft.Sql/servers/firewallRules",
            "apiVersion": "2014-04-01",
            "name": "[format('{0}/AllowAll', parameters('serverName'))]",
            "dependsOn": [
                "[resourceId('Microsoft.Sql/servers', parameters('serverName'))]"
            ],
            "properties": {
                "startIpAddress": "0.0.0.0",
                "endIpAddress": "255.255.255.255"
            }
        }
    ]
}
```

5. In the next screen:

- Select the only option in the `Resource group` drop-down box.
- Then decide on a name for the `Administrator Login` and `Administrator Login Password` and write down what you chose. Make sure the Login name is not too short, and it's a good habit to always create strong passwords[^20]. Then click `Review & Create` followed by clicking `Create` and your deploymentℹ️ will begin. This will take around 5 minutes.

[^20]: Strong password guidance: <https://learn.microsoft.com/en-us/sql/relational-databases/security/strong-passwords?view=sql-server-ver16>

> ℹ️ While it deploys, note you have just deployed a cloud PaaS resource using a template where its size, location, and IP access rules are already specified for you. You learned about PaaS in your first e-learning module. The template is written in JSON, a universal data format ideal for specifying cloud resource attributes. Its readable yet structured nature enables precise and automated cloud provisioning. Follow this link to see the structure of the JSON file visualised:
<https://jsoncrack.com/editor?json=https://raw.githubusercontent.com/Corndel/corndel-datasets/main/azure_arm_templates/ARM-template-azure-sql-db-and-server.json>

5. When you see the message `Your deployment is complete`, click on the `Go to your resource group` blue button. Then, select the Adventureworks database you should see in the list (as shown below).

| ![select](/images/select.png) |
|:--:|

6. For the database, on the left hand side, click on the `Query editor` button and type in the Administrator  password you wrote down earlier.

| ![adventure](/images/adventure.png) |
|:--:|

7. Once logged in, expand the `Tables` on the left-hand side and right-click on the `customer` table and select `Select Top 100 rows`. This populates your code window with SQL and runs it so that you see the customer data.

| ![query](/images/query.png) |
|:--:|

> ℹ️ In larger organisations, a data engineer may be less likely to create resources for live production use and instead, it would be the responsibility of more specialised roles such as DevOps engineers or cloud architects. These professionals often have deeper expertise in managing production environments, ensuring high availability, scalability, and compliance with regulatory requirements. However, it is still a useful skill to build resources in development environments, but remember, these are not suited for production due to security risks. For production, stringent security measures are necessary to protect sensitive data and comply with industry standards. This includes implementing strong firewall rules, data encryption (both in transit and at rest), and regular access and activity audits. For a detailed guide on best practices, particularly for a production setup, refer to: [Azure SQL Database Security Best Practices](https://learn.microsoft.com/en-gb/azure/azure-sql/database/security-best-practice?view=azuresql).

<a id="azureVM"></a>

### 💻9️⃣ Setup a windows server VM in your Azure sandbox

Due to the way that the organisation's networking is setup it is not possible to connect directly to SQL servers outside of the corporate network. If using a work computer, you need to setup a virtual machine to install the tools in the next section on. That way the instructions in [section 10](#tools) will work as written.

1. In your Azure sandbox that you set up in the previous section. Return to the [home](https://portal.azure.com/home) screen and click the Virtual Machines icon in the azure services section at the top of the page.

2. In the Virtual Machines page click the blue Create icon.

3. In the following page, select the available resource group e.g. `1-12345adfe-playground-sandbox`

4. Choose a name for your machine -- it does not matter what it is e.g. MyVirtualMachine, Fred, OptimusPrime.

5. Select `Windows Server 2022 Datacenter: Azure Edition Hotpatch - x64 Gen2` for the Image.

6. Select a username and password - use a complex password (12 characters, 1+ capital, lowercase, symbol, number) or Azure gets grumpy

All the other default options are fine. 

7. Once the VM is deployed you can connect to it using Remote Desktop Protocol - as we did in the morning session. Select the Public IP address from the Azure Sandbox for the computer's name in RDP.

If you follow the instructions in the "tools" section, but install software on this new virtual machine you should not have any connectivity issues.


<a id="tools"></a>

### 💻9️⃣ Query your database with MS recommended tools (~20 mins)

[Back to Contents](#contents)

Finally, let's now experiment with different ways to connect to the Azure SQL instance beginning with the Azure recommended tool list[^21].

Below, we suggest three ways you could connect. Note that none of these SQL tool connection methods will connect if you install the necessary software on your ACG Windows VM. This means you would need to have the SQL tool installed on another machine, such as your work laptop, a personal laptop, or any device with internet access. Or if this is still not possible or delayed, as described above, you can still run SQL from within the Azure web portal to complete the going further SQL exercise below.

---
> ❓SQL Tools and Dialects Discussion:
Discuss in your group any prior experience with SQL tools and dialects from various vendors. Share your thoughts on:

1. The SQL dialects you have used (e.g., T-SQL, MySQL, PL/SQL).
2. The specific SQL tools you've worked with for each SQL variant.
3. Any learning goals you have for SQL (e.g., to learn a particular SQL skill or technique).

| Vendor          | SQL Dialect        | Main SQL Tool                  |
|-----------------|--------------------|--------------------------------|
| Microsoft       | T-SQL              | SQL Server Management Studio   |
| Oracle          | PL/SQL             | Oracle SQL Developer           |
| PostgreSQL      | PostgreSQL         | pgAdmin                        |
| MySQL           | MySQL              | MySQL Workbench                |
| IBM             | SQL PL             | IBM Data Studio                |
| SQLite          | SQLite             | DB Browser for SQLite          |
| MariaDB         | MariaDB SQL        | HeidiSQL, DBeaver              |
| SAP             | SAP HANA SQLScript | SAP HANA Studio                |
| Amazon          | PartiQL (for DynamoDB) | Amazon DynamoDB Console   |
| Google          | BigQuery SQL       | Google Cloud Console           |
| Snowflake       | Snowflake SQL      | Snowflake Web Interface        |
| Teradata        | Teradata SQL       | Teradata Studio                |
| MongoDB         | MongoDB Query Language | MongoDB Compass            |
---

To connect to your Azure sandbox from each of the three tools described below, first find the database in the overview section in Azure and copy the `Server name` shown below in the red box:

| ![servername](/images/servername.png) |
|:--:|

[^21]: Recommended tools: <https://learn.microsoft.com/en-gb/sql/tools/overview-sql-tools?view=sql-server-ver16#recommended-tools>

1. **Azure Data Studio**

1️⃣ Download and install Azure Data Studio using this link: <https://learn.microsoft.com/en-us/azure-data-studio/download-azure-data-studio?view=sql-server-ver16&tabs=win-install%2Cwin-user-install%2Credhat-install%2Cwindows-uninstall%2Credhat-uninstall#download-azure-data-studio>

Then, click on the `Create a connection` tile. In the dialog that appears on the bottom right: 1) Copy the server name from Azure and past it into the Server box 2) Select the login type of `SQL Login` 3) Enter your login details for the Azure SQL S server, 4) You can also select the `Adventureworks` database as the default database.

| ![ads](/images/ads.png) |
|:--:|

2️⃣ Once connected, you will see the tables of the `Adventureworks` and you can click on the three dots to the right of the `Customer` table and then click on `Select Top 1000` rows.

| ![ads](/images/adsrows.png) |
|:--:|

1. **VS Code extension**

1️⃣ Install the SQL server extension[^22] from this link: <https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql> or add the VS code extension as follows

1. In VS Code, click on the Extensions view icon
2. Search for `sql server` in the search box
3. The `SQL Server (mssql)` should be the top search result from where you can click on its `install` blue button.

| ![ads](/images/mssql.png) |
|:--:|

2️⃣ In VS Code, create a new text file from the File Menu (it's the top option). In the blank new text file, copy and paste in the SQL code below and save it with the name `ExploreAdventureworks.sql`

```sql
SELECT * 
FROM SalesLT.Customer;
```

| ![ads](/images/vscodesql.png) |
|:--:|

3️⃣ To connect, click the play button shown then select `+ Create connection profile`, then paste in sever name from Azure and the other details when prompted, which are 1) The default database of `Adventureworks`, 2) Select the `SQL Login`` option, 3) Then enter the admin username and password you gave to the SQL server earlier.

[^22]: Guide to getting started with the mssql extension in VS Code:  <https://learn.microsoft.com/en-us/sql/tools/visual-studio-code/mssql-extensions?view=sql-server-ver16#getting-started-with-the-mssql-extension-in-vs-code>

3. **Microsoft SQL Server Management Studio (SSMS)**

1️⃣ From this web page, click on the `Free Download...` link at the top of the page to download and then install SSMS: <https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16&redirectedfrom=MSDN#download-ssms>

2️⃣ In SSMS, 1) Paste the the server name from your Azure sandbox into the `Server name:` box 2) From the `Authentication:` drop-down box select `SQL Server Authentication` 3) In the final two boxes, enter the admin username and password you gave to the SQL server earlier.

| ![ssms](/images/ssms.png) |
|:--:|

3️⃣ You can now expand the tree on the left, then right-click on a table and select the  `Select top 1000 rows` option to test if data can be returned.

| ![ssms](/images/ssmsopen.png) |
|:--:|

## 🎉 If you have completed all the 💻 activities up to this point, congratulations! If time allows before the end of the workshop, continue with the 🚀 going further activity below

<a id="know"></a>

### 🚀1️⃣0️⃣ Get to know your data with simple SQL (~60 mins +)

[Back to Contents](#contents)

In our next workshops, we will explore SQL skills in more detail in the context of data engineering.

What should not be underestimated is the value of becoming familiar with your source data and its structure so that you can effectively query, manipulate, and extract meaningful insights from it. Understanding the nuances of your data is key to developing efficient queries and making informed decisions based on that data.

A surprisingly quick way to do that is to open each table and eyeball its contents and ask yourself simple questions. So as a final exercise, if time allows, follow the steps below.

<details><summary>If time allows</summary>

1️⃣ In your SQL tool of choice (e.g. the Azure Portal, Azure Data Studio, the VS Code extension, or SSMS) open the first few rows of just the tables that sounds like they hold the key information in the database. For example:

```sql
SELECT * 
FROM SalesLT.Customer;
```

```sql
SELECT * 
FROM SalesLT.Product;
```

```sql
SELECT * 
FROM SalesLT.SalesOrderHeader;
```

```sql
SELECT * 
FROM SalesLT.SalesOrderDetail;
```

2️⃣ For each table you open, write down or mentally note:

- What type of information does this table predominantly contain? Try to summarise the table’s purpose or role within the database in a sentence or two.
- Identify the column or set of columns that uniquely define each row. Consider how these identifiers are structured – are they numerical, textual, or a combination? How do they interact with other tables? This understanding is crucial for linking tables.

</details>

<a id="next"></a>

## 12 Preparation for next workshop

[Back to Contents](#contents)

| ![aptem](/images/aptem.png) |
|:--:|

In our workshop next month, we will start to build on your SQL skills and be covering advanced SQL transformations that are often used and are valuable in Data Engineering. Please make sure you have done the following before that workshop.

1. If not already done, complete Aptem modules `1.1 The Uses of Cloud Computing Platforms` and `1.2 Data engineering in your organisation`
and the Data Engineer Pass Descriptor CPD questions after them.

2. The next workshop is a detailed SQL workshop. Complete SQL modules 2.1 and 2.3 beforehand that are SQL-focussed.

3. To keep on track with your general data engineer learning, also complete modules `2.2 Data normalisation for data integrity` and `2.4 Data store types and optimisation` and the Data Engineer Pass Descriptor CPD questions after them.