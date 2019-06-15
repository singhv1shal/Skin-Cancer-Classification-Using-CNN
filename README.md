# Skin-Cancer-Classification-Using-CNN
## Lesions Detection:
 Vishal Singh (singhvishal0304@gmail.com)

## Dataset
This model is trained over MNIST HAM10000 dataset link: https://www.isic-archive.com/#!/onlyHeaderTop/gallery which contains lesions with multiple images, which can be tracked by the lesion_id-column within the HAM10000_metadata file. The data is splitted into train and test set with 80/20 ratio. The model classifies the lesions detected into the seven categories : Actinic keratoses and intraepithelial carcinoma / Bowen's disease (akiec), basal cell carcinoma (bcc), benign keratosis-like lesions (solar lentigines / seborrheic keratoses and lichen-planus like keratoses, bkl), dermatofibroma (df), melanoma (mel), melanocytic nevi (nv) and vascular lesions (angiomas, angiokeratomas, pyogenic granulomas and hemorrhage, vasc).

## Model
The model use Convolutional Neural Networks. The starting two layer and last layers contain 32 filters and 64 filters respectively. Model uses drop-out three times to avoid overfitting. Maxpooling is used 2 times to downsample the image. All intermediate layers use relu activation and final layer uses softmax activation.

## Implementational Details
Keras is used to implement the CNN. The model is trained on Google Colab which uses K80 GPU. The learning rate is started with a larger value then gradually decreased over time. This is due to the intuition to explore loss function in deep.

## Result
The model has 92.8 % accuracy on test data.

## Future Scope
This problem can also be approached with 2 stage Machine Learning Method. Image processing techniques can serve in data processing and feature extraction. Artificial Neural Network can be used as the second stage for the lesions detection. The comparison between results of both the approach may give novel instincts.
