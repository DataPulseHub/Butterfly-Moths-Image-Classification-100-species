
# A model for classifying photos of butterfly and moth species

Data comes from: <https://www.kaggle.com/datasets/gpiosenka/butterfly-images40-species?datasetId=456014>
Validation data set for 100 species of butterflies or moths. All images are **224 X 224 X 3** in JPG.
The train set consists of **12594** images representing **100** subdirectories, one for each species.
The test set consists of **500** images representing **100** subdirectories with **5** test images per genre.
Valid set of **500** images available on 100 subdirectories with 5 images for environment validation.
CSV files included. The butterflies and moths .csv file consists of **4** columns with **13595** lines. First line for header, remaining lines for each image file in train, test and validation dataset,
Columns for classic ID, file for files, label and dataset. The filepaths column contains a valid image relative.
The label column contains the textual species label associated with the image files. A data set column describing which data sets (train, test, or valid) should be included. The class ID column contains the numeric class index for the image file.

**Layer architecture:**

1. Convolutional layer (Conv2D) with 64 filters that transform the input image.

2. MaxPooling layer, which reduces the dimensionality of the image while preserving the most important features.

3. Dropout layer which helps prevent the network from overfitting by randomly ignoring a certain number of neurons during training.

4. Second convolutional layer (Conv2D) with 128 filters.

5. Second layer of MaxPooling.

6. Second Dropout layer.

7. Flatten layer, which flattens the data into a one-dimensional vector.

8. Dense layer with 512 neurons that performs classification based on features extracted by previous layers.

9. Third layer Dropout.

10. Final dense layer (Dense) with 100 neurons that predicts the probability of the image belonging to each of the 100 species.

# Conclusions:

Analyzing these results, the following trends can be noticed:

- The loss on the training and validation set decreases as the epochs progress, which indicates that the model is able to adapt to the training data and generalize to the validation set.

- Accuracy on the training set also increases as epochs progress, indicating that the model is better at classifying the training data.

- However, accuracy on the validation set does not always increase as epochs progress. At some epochs, the accuracy on the validation set is lower than the accuracy on the training set, suggesting some level of model overfitting.
