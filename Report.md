**Report- SOI-Auburn Waves:**

Since the task given was of image detection, I used open CV for image reading/processing and InceptionV3(a CNN) for predicting labels.

Preprocessing included removing the rows of image data in train.csv which did not even exist in the train dataset(images folder), and converting of categorical classes into numerical ones for easy training.
 
Batch size alterations, learning rate scheduler, training on different epochs were required to minimise the huge loss and poor accuracy in the beginning.

The resultant best validation accuracy peaked at 70%, validation loss=0.87    [batch size=16, epochs=15]

The model was finally uploaded to the test dataset but resulted in some error.
The predicted labels all consisted of the label 'other' which is clearly due to the majority of its occurrence in train_dataset. Data augmentation and class weights were applied but it did not help much.
