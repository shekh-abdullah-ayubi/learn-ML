# learn-ML
Have a proper handson session across each concepts behind ML and DL

## Here is a step-by-step guide to coding and running ML scripts in a Codespace, complete with Jupyter notebook support

### Step 1: Create a new repository and add a dev container

1. Log in to GitHub, click the + icon, and select New repository. Give it a name (e.g., Learn-ML). 
You can choose to make it public or private.

2. Launch a codespace. From your new repository page, click the green < > Code button, then go to the Codespaces tab and click Create codespace on main.

3. Add dev container configuration. Once the codespace is loaded, open the Command Palette ( Ctrl+Shift+P or Cmd+Shift+P ). Type add dev and select Codespaces: Add Dev Container Configuration Files

### Step 2: Customize the devcontainer.json file

1. Open the file at .devcontainer/devcontainer.json.

2. Add a settings property to tell VS Code to use the Python interpreter from the virtual environment by default.
3. Modify the postCreateCommand to:
    3.1. Create the MLenv virtual environment.
    3.2. Install the dependencies from your requirements.txt file into MLenv.

4. Specify the location of the MLenv virtual environment in the python.defaultInterpreterPath setting.

### Step 3: Create the requirements.txt file

### Step 4: Rebuild the Codespace
After saving the devcontainer.json and requirements.txt files, you need to rebuild the Codespace for the changes to take effect. 

1. Open the Command Palette (Ctrl+Shift+P or Cmd+Shift+P).

2. Run Codespaces: Rebuild Container. 

During the rebuild, Codespaces will execute the postCreateCommand, creating the MLenv virtual environment and installing all dependencies within it

### Method 2: Manually activate virtual env and install modules
1. create the virtual environment using python -m venv

        python3 -m venv MLenv
2. Activate the new environment
        
        . MLenv/bin/activate
3. Install the dependencies

        pip install -r requirements.txt

