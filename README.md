# Freshness_Detection_Of_Fruits


Detecting freshness of fruits like apples, oranges and bananas. The dataset is taken from [Fruits fresh and rotten for classification](https://www.kaggle.com/sriramr/fruits-fresh-and-rotten-for-classification). The dataset containes ~2700 images of fresh and rotten fruits for classification. The code uses VGG16 model for transfer learning to classify the fruit images as fresh or rotten. 


## Getting Started

Clone the project repository to your local machine, then follow up with the steps as required.

### Requirements

After cloning the repository, install the necessary requirements for the project.
```
pip install -r requirements.txt
```

### Training

The fruits.h5 file is pre-trained in the images from the [Fruits fresh and rotten for classification](https://www.kaggle.com/sriramr/fruits-fresh-and-rotten-for-classification). If you wish to train the model from scratch on your own dataset, prepare your dataset in the following way:
1. Load the images in the "*images*" folder
2. Store the images into the subdirectory of their class-names. Example: if image fresh_apple_01.jpg belongs to the class "Fresh_Apple" then the directory of that image should be /images/Fresh_Apple/fresh_apple_01.jpg

You can then train the model by using the train.py file
```
python train_model.py --dataset dataset --model fruits.h5
```

The plot for Training and Validation Loss and Accuracy.

### Testing

To test the model, use the test_model.py file. 
```
python test_model.py --model fruits.h5 --labelbin lb.pickle --image test/freshApple_1.png
```

You need to pass some parameters for the test_model.py file:
1. --model: path to trained model <br>
2. --labelbin: path to label binarizer <br>
3. --image: path to input image <br>

## Contributing
If you would like to contribute to this project, please submit a pull request. We welcome contributions from the community!

License
This project is licensed under the MIT License - see the LICENSE file for details.


## Acknowledgments

We would like to thank the open source community for their contributions to this project.
