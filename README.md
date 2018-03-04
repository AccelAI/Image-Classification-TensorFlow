# Image-Classification-TensorFlow

## Installation

Step-by-step guides for running the code in this repository can be found in the [workshop installation guides](https://github.com/AccelAI/AI-Workshop-Installation-Guides) directory.

If you already have Tensorflow installed on your local machine either directly or through an Anaconda distribution, simply clone this repository in your prefered directory, cd into the cloned directory, and type `jupyter notebook` to get started (it will appear in a new browser window or tab).

If you are not able to launch Jupyter Notebook inside your TensorFlow virtual environment execute the following once inside this project directory:

`pip install ipykernel
python -m ipykernel install --user --name=my-virtualenv-name`

**Replace "my-virtualenv-name" with the name of your environment.**

## Following the Lab

1. Begin on the Hello World notebook to make sure TensorFlow is installed and functioning properly in your environment.

2. Once you've verified TensorFlow is running currectly, open the TensorFlow for Poets Codelab notebook and follow the instructions to train mobilenet on flower data.

Execute this code in a seperate terminal window from your jupyter notebook. 

If you are using TensorFlow in Docker, run the following command to access the docker bash shell:

`docker exec -it tf /bin/bash`

3. Once you've successfully trained the classifier to recognize flower data, we'll modify the image paths to train on the cephalopod data i've included in this repository.

4. Scrape Google for image data of your own categories using a [Google Image Scraper](https://github.com/quickresolve/img-scrapers)

5. Train the classifier on your new data set!!
