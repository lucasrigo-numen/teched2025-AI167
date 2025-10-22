
# Hands-On Setup

Before you can get started you first need to set-up you workshop environment:
- [Hands-On Setup](#hands-on-setup)
  - [Step 1: Setup Python Environment](#step-1-setup-python-environment)
    - [1.1 Open Visual Studio code and clone Git Repo](#11-open-visual-studio-code-and-clone-git-repo)
    - [1.2 Configure connection details for AI Core](#12-configure-connection-details-for-ai-core)
    - [1.3 Create a Python virtual environment](#13-create-a-python-virtual-environment)
  - [Step 2: Setup Bruno Environment](#step-2-setup-bruno-environment)
    - [Object Store Services Key](#object-store-services-key)
- [Summary](#summary)

## Step 1: Setup Python Environment
For the Hands-on Session we will use **Visual Studio Code** to to run our pyton code. 

### 1.1 Open Visual Studio code and clone Git Repo

Open "Visual Studio Code" on your laptop. 
<p>
<img src="images/vsc.png" alt="Visual Studio Code" width="60"/>
</p>

Once you opened your Visual Studio Code, you will see the **Welcome** tab. In this Welcome tab select under the **Start** section the option ```Clone Git Repository ``` to clone this Git repository with the excercises using the following URL  
```sh
https://github.com/SAP-samples/teched2025-AI167.git 
```
Paste the URL into the command pallett at the top of the window and press enter. 
<p>
<img src="images/clone_repo.png" alt="Visual Studio Code" width="900"/>
</p>

Select and local directory on your laptop ( e.g. desktop) into which you want to clone the project then select ```Select as Repository Destination ```
<p>
<img src="images/select_dest.png" alt="Visual Studio Code" width="900"/>
</p>

When you receive the notification asking if you want to open the cloned repository, select ```Open```.
If everything was successful you should see the following folder structure in your Explorer:
<p>
<img src="images/success_repo.png" alt="Visual Studio Code" width="900"/>
</p>

### 1.2 Configure connection details for AI Core 
For this Hands-on Session we will use the grounding service on AI Core. 
To interact with AI Core, we need to get the service keys and add it to our python enivornment.
The serivce keys you will get in the BTP cockpit in the respective service instance, as described in the next steps. 


For the hands-on Session we provided seperate [BTP Subaccounts](https://emea.cockpit.btp.cloud.sap/cockpit/?idp=tdct3ched1.accounts.ondemand.com#/globalaccount/4c772782-0751-42ee-93c3-897452fdcb63&//detail/862bffe2-c93b-4314-beef-18ccd09393b3/?layout=TwoColumnsMidExpanded-) for you. 
Please log in with your username and password provided in the workshop room and click on continue.

<p>
<img src="images/btp_login.png" width="900"/>
</p>

Once you successfully logged in, you will be redirected to the BTP Cockpit. To see the list of subbaccount you need to click on **Account Explorer**.

➡️ Next click on the tile of your respective subbacount **AI167_XXX**.
<p>
<img src="images/access_subaccount.png" width="900"/>
</p>


➡️ Got to  **Instances and Subscription** and open the SAP AI Core Instance's **credentials**. 

<p>
<img src="images/copy_json.png" width="900"/>
</p>

➡️ Click **Copy Json**

➡️ Return to Visual Studio Code and create a new file ```.aicore-config.json```in the ```TECHED2025-AI167``` directory. 
<p>
<img src="images/new_file.png" width="900"/>
</p>

➡️ Paste in the service key into ```TECHED2025-AI167/.aicore-config.json```, which should look similiar to the following.
<p>
<img src="images/config_file.png" width="900"/>
</p>

➡️  Save the file. 


### 1.3 Create a Python virtual environment 
➡️ Start a new Terminal 
<p>
<img src="images/open_terminal.png" width="900"/>
</p>

➡️ Create a virtual environment using the following command:
```python
python3 -m venv ai167env --upgrade-deps
```
Activate the virtual environment ```ai167env``` like this and make sure it is activated.  
```python
source ai167env/bin/activate
```
<p>
<img src="images/env_active.png" width="900"/>
</p>

## Step 2: Setup Bruno Environment


### Object Store Services Key 
-- To Do: Click path to object store service key




# Summary

Now everything is ready to start the excercises. 

For the next excercise continue in Visual Code.

Continue to - [Exercise 1 - Get Started with Grounding ](ex1-grounding-basics.ipynb)
