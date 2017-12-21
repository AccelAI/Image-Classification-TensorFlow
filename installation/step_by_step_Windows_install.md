# Setting up Docker and TensorFlow for Windows

## Installing Docker

Docker is a system to build self contained versions of a Linux operating system running on your machine. When you install and run TensorFlow via Docker it completely isolates the installation from pre-existing packages on your machine.

**Windows 10 or newer:**

1. Download the Docker installer [here](https://download.docker.com/win/stable/InstallDocker.msi).

2. Run ‘InstallDocker.msi’

3. Launch Docker when the installer finishes

If Docker warns you about Hyper-V not being enabled, allow Docker to enable Hyper-V and automatically restart your machine

4. Open PowerShell or ‘cmd.exe’ and run the Docker hello-world image to ensure Docker is working properly

`docker run hello-world`

**Windows 7**

The legacy solution for older Windows systems is Docker Toolbox.

https://docs.docker.com/toolbox/toolbox_install_windows/

Click on the "Get Docker Toolbox for Windows" button. 

Follow their instructions to install Docker and to make sure that virtualization is enabled on your machine.


## Installing TensorFlow

1. Open PowerShell

2. Pull the tensorflow docker image:

` docker pull tensorflow/tensorflow` 

3. Test running the Docker TensorFlow image:

`docker run -it -p 8888:8888 tensorflow/tensorflow`

4. Copy the URL with your login Jupyter login token from PowerShell and go to it in your web browser

If you were able to access the page, Docker and TensorFlow have been installed correctly.

## Connecting & Launching the TensorFlow Lab

Note: For this lab, we are cloning the Image-Classification-TensorFlow repo to the root of our C: drive, you can put it anywhere you like, but the rest of the tutorial will assume it is located at:

`C:\Image-Classification-TensorFLow\`

1. Clone the github repo https://github.com/AccelAI/Image-Classification-TensorFlow.git

2. Enable sharing of the drive you cloned the repo to in Docker

    - Right Click on the Docker System Try icon.
    - Click ‘Settings’
    - Go to ‘Shared Drives’ and check the box for the drive is located on.
    - Click ‘Apply’

3. Open a **new** PowerShell

4. Run the TensorFlow docker image and mount the notebooks.

`docker run -it -p 8888:8888 -p 6006:6006 -v //c/Image-Classification-TensorFLow-master:/notebooks tensorflow/tensorflow`

5. In your browser, navigate to URL provided by Docker inside of PowerShell

6. Ensure that the notebooks for the lab are available.

7. Return to the lab [README](../README.md) for further instructions.
