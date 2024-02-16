# Overiview

This project uses neural networks transfer learning in tensorflow to build an image classifier for emotions of dogs. The dataset is from [Kaggle](https://www.kaggle.com/datasets/danielshanbalico/dog-emotion) which contains 4000 images in total, 1000 in each of the 4 classes - angry, happy, relaxed, sad.

This notebook should be run in Google Colab using GPU, the dataset is directly loaded from Kaggle API - a Kaggle token username and password is needed.

## Model Strategies:
- InceptionV3 and VGG16 were both explored as pre-trained feature extracters.
- Global Average Pooling was utilized to reduce dimensions prior to the dense layers.
- Data augmentation and Dropouts were utilized to regularize.
- Model checkpoints were also used to save the best model accross different epochs which can be used to import and train further.

### Repository Navigation: The main notebook is best run in Google Colab, the dataset is not contained within the repo but was imported directly via Kaggle's API to Google Colab

## Conclusion: 
- VGG 16 works better than Inception V3 in this particular case. A less complex model as features extractor is better as important features are concentrated in a dog’s face instead of the full image
- Next we can try visualizing feature extractions in the convolutional layers to tune further






