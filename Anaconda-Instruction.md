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