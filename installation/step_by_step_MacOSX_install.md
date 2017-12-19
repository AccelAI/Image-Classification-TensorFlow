# Installation Instructions for MacOSX

## Install

1. Open the Terminal Application - using spotlight search (by pressing the **cmd** + **space bar** simultaneously and typing terminal) or through your gui [like this](https://www.wikihow.com/Open-a-Terminal-Window-in-Mac)

2. To install in your home directory:
	* Type `cd ~` into the command-line prompt and 
	* *Execute* the line by pressing the **return** key on your keyboard

3. Retrieve all of the code for this workshop by executing `git clone https://github.com/AccelAI/Image-Classification-TensorFlow.git` (if you haven't used `git` before, you may be prompted to install Xcode -- do it!)

4. Install the Docker "Stable channel" (if you are already using an older version of Docker and run into installation issues downstream, try updating to the latest version of Docker)

For Mac OS - https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac

Click on the "Get Docker for Mac (Stable)" button as pictured below.

![Docker Stable](/imgs/docker-stable.png)

Docker is a system to build self contained versions of a Linux operating system running on your machine. When you install and run TensorFlow via Docker it completely isolates the installation from pre-existing packages on your machine.

5. Start Docker, e.g., using spotlight search (by pressing the cmd + space bar) or Finder to navigate to your Applications folder and double-clicking on the Docker icon

6. Download TensorFlow by executing `docker run -it gcr.io/tensorflow/tensorflow:latest-devel`

7. Check your installation of TensorFlow in the Docker container - in the terminal execute the following: 
    
    ````
    $ python
    ...
    >>> import tensorflow as tf
    >>> hello = tf.constant('Hello, TensorFlow!')
    >>> sess = tf.Session()
    >>> print(sess.run(hello))
    Hello, TensorFlow!
    >>> a = tf.constant(10)
    >>> b = tf.constant(32)
    >>> print(sess.run(a + b))
    42
    >>>

    ````

8. Open a new terminal window by pressing **cmd** + **t** and move into the workshop directory by executing `cd Image-Classification-TensorFlow`


9. Link this directory to your Docker container by executing `docker run -it --rm --name tf -v ~/Image-Classification-TensorFlow:/notebooks/ -p 8888:8888 -p 6006:6006 tensorflow/tensorflow`


You can access the bash in your Docker container through the terminal by executing this command instead: 

`docker run -it --rm --name tf -v ~/Image-Classification-TensorFlow:/notebooks/ -p 8888:8888 -p 6006:6006 tensorflow/tensorflow /bin/sh`

More details on sharing files from your local machine into a Docker container can be found here: https://github.com/rocker-org/rocker/wiki/Sharing-files-with-host-machine

10. Click the link in your terminal while holding down the **cmd** key to launch Jupyter in your browser

11. Return to the lab [README](../README.md) for further instructions.


## Shutdown

You can shutdown the Jupyter notebook by returning to the Terminal session that is running it and hitting the **ctrl** and **c** keys simultaneously on your keyboard.


## Restart

You can restart the Jupyter notebook later by following steps nine and ten alone.
