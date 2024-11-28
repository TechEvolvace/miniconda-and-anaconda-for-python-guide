# Instructions for Installing Anaconda Distribution

## Step 1: Download Anaconda (Only if you don't have Anaconda installed yet)

1. **Visit the Anaconda Website**:
   - Go to the [Anaconda distribution page](https://www.anaconda.com/products/distribution).

2. **Choose the Version**:
   - Select the version appropriate for your operating system (Windows, macOS, or Linux).

3. **Download the Installer**:
   - Click on the installer link to download the Anaconda installer for your system.

## Step 2: Install Anaconda (Only if you don't have Anaconda installed yet)

1. **Run the Installer**:
   - Locate the downloaded installer file (usually in your Downloads folder) and run it.

2. **Follow the Installation Wizard**:
   - **Welcome Screen**: Click "Next" to continue.
   - **License Agreement**: Read and accept the license agreement, then click "Next."
   - **Installation Type**: Choose whether to install for "Just Me" (recommended) or "All Users." Click "Next."
   - **Choose Installation Location**: Select the destination folder for Anaconda (the default is usually fine), then click "Next."
   - **Advanced Installation Options**: You may see options to:
     - **Add Anaconda to my PATH environment variable**: *Not recommended* as it can lead to conflicts.
     - **Register Anaconda as my default Python**: Recommended if you want Anaconda to be the default Python version.
     - **Clear the package cache upon completion**: Recommended for saving disk space.
   - Choose your preferences and click "Install" to start the installation.

3. **Complete the Installation**:
   - Once the installation is finished, you can choose to launch Anaconda Navigator or the Anaconda Prompt. Click "Next" and then "Finish" to close the installer.

## Step 3: Verify the Installation

1. **Open Anaconda Prompt**:
   - Search for "Anaconda Prompt" in your Start menu (Windows) or use the terminal (macOS/Linux).

2. **Check Anaconda Version**:
   - In the Anaconda Prompt, type the following command:
     ```
     conda --version
     ```
      - This same command automatically works with Command Prompt and Window Powershell
      - If configured with Git Bash by adding important paths to specific Anaconda folders into Git Bash's file `.bashrc`, then this same command can work on Git Bash too! More info on bottom of this Markdown file!
      - You should see the installed version of Anaconda.

## Step 4: Update Anaconda (Optional)

- To ensure you have the latest packages, run the following command in the Anaconda Prompt:
  ```
  conda update conda
  ```
   - This same command automatically works with Command Prompt and Window Powershell
   - If configured with Git Bash by adding important paths to specific Anaconda folders into Git Bash's file `.bashrc`, then this same command can work on Git Bash too! More info on bottom of this Markdown file!

## Step 5: Create and Manage Environments

1. **Create a New Environment**:
   - You can create a new environment for your projects using:
     ```
     conda create --name <env_name> python=3.x
     ```
      - Replace `<env_name>` with your desired environment name and `3.x` with the version of Python you want.
      - This same command automatically works with Command Prompt and Window Powershell
      - If configured with Git Bash by adding important paths to specific Anaconda folders into Git Bash's file `.bashrc`, then this same command can work on Git Bash too! More info on bottom of this Markdown file!

2. **Activate the Environment**:
   - To activate your new environment, use:
     ```
     conda activate <env_name>
     ```
      - This same command automatically works with Command Prompt and Window Powershell
      - If configured with Git Bash by adding important paths to specific Anaconda folders into Git Bash's file `.bashrc`, then this same command can work on Git Bash too! More info on bottom of this Markdown file!

3. **Deactivate the Environment**:
   - To deactivate the active environment, simply run:
     ```
     conda deactivate
     ```
      - This same command automatically works with Command Prompt and Window Powershell
      - If configured with Git Bash by adding important paths to specific Anaconda folders into Git Bash's file `.bashrc`, then this same command can work on Git Bash too! More info on bottom of this Markdown file!

## Summary 
- If you don't have Anaconda installed yet, download and install Anaconda.
- Follow the installation wizard and set your preferences.
- Check if you have Anaconda installed

### Workflow with Anaconda in your Python projects
- Create a new environment with Anaconda in your specific Python project, only if you haven't created the environment yet. 
 - It's possible to create separate environments for your differnt Python projects! 
```
   conda create --name <env_name> python=3.x
```
 
- Only if you have Anaconda environment in your Python project created AND you want to start working on your Python project, activate the environment 
```
   conda activate <env_name>
```

- Only if you have Anaconda environment in your Python project created AND you want to take a break from your Python project, deactivate the environment 
```
   conda deactivate
```

## Setting up Anaconda to work with Git Bash
Git Bash doesn't automatically add the path to important files and folder for Anaconda, so when you run 
```
   conda --version
```
or any other conda command with Git Bash, you may get the error `bash: conda: command not found`

So you need to manually configure Git Bash to work with Anaconda
1) Check if you have Git Bash's configuration file `.bashrc` somewhere in your local computer
2) If not, create a new `.bashrc` file. If you do, skip to step 3. 
3) Run this to open the new `.bashrc` file in Terminal (or you can also open this in VSCode)
```
   nano ~/.bashrc
```

4) Add these paths to Anaconda's bin, Scripts, and condabin folder in the `.bashrc` file: 
``` 
   export PATH="/c/Users/<YourUser>/Programs-Installed/Anaconda3/bin:$PATH"
   export PATH="/c/Users/<YourUser>/Programs-Installed/Anaconda3/Scripts:$PATH"
   export PATH="/c/Users/<YourUser>/Programs-Installed/Anaconda3/condabin:$PATH"
```

5) If you are opening the `.bashrc` file in Terminal through `nano ~/.bashrc` command: 
 - Save the new changes with `CTRL + O` then press `Enter`
 - Press `Ctrl + X` to exit nano 

6) Apply the new changes with Git Bash:
``` bash
   source ~/.bashrc
```

7) Check if Anaconda is successfully configured with your Git Bash by running in Git Bash: 
``` bash
   conda --version 
```

If it loads up the conda version, then you successfully configured Anaconda to work with Git Bash! 

If not, take a look again at the instruction above. 