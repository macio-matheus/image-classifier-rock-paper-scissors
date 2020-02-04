## Image Classifier Rock, Paper e Scissors dataset

By: Mácio Matheus Santos de Arruda

Multilabel classification using convolutional networks. This project uses the dataset Rock, Paper e Scissors, a famous database for computer vision applications.

------

### The dataset

Rock Paper Scissors contains images from a variety of different hands,  from different races, ages and genders, posed into Rock / Paper or Scissors and labelled as such.

![Pie](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/pie.jpg)

![hist](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/data_hist.png)


### The CNN Summary

Using Keras, the neural network below was assembled to solve the presented classification problem:

![CNN](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/network_summary.png)


### Train / Validation Split

As in the image, for the validation set that compose the metrics measured in the training, a percentage of 33% of the data in the training images folder is defined in the Keras generator by the parameter validation_split.

Note: The Live Test is performed with a set of images that do not participate in the training.

![Params](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/train-test.png)


### Results Loss and Accuracy

Below is the graph of loss and accuracy in training and validation sets during training

![loss_and_accuracy](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/loss_acc_plt.jpg)


### Test live

Prediction performed on images that were outside the training set and validation. The crabs were intentionally pointed in circle format to cause error in the model:

![result](https://raw.githubusercontent.com/macio-matheus/image-classifier-rock-paper-scissors/master/docs/result.png)


#### Usage

First of all, build the container using docker-compose and then you can 
access the Jupyter that is ready to be used.


#### Run with docker compose

```sh
cd image-classifier-rock-paper-scissors
docker-compose up -d
```

#### Accessing Jupyter
```sh
http://<your-ip>:8111/tree
```

#### Ports

```sh
    - 8888 => Jupyter
    - 6011 => Tensorboard
    - 5011 => App
```

### DockerHub

```sh
https://hub.docker.com/r/maciomatheus/jupyter_notebook_data_science/
```
