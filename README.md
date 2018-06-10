# Deep whales

## Abstract
Classifying [whale sightings] with CNNs. 

## Workflow
PREPROCESSING
* Visualize a few whales just for fun. [Cronopio All]
* Check images color schema. If not consistent, greyscale everything. [Cronopio All]
* Check average image size + std. [Cronopio All]
* Rescale all images accordingly. [Cronopio All]
* Normalize image intensity on single grayscale channel.
* Build an algorithm to crop whales' tail from background (looks like a problem within the problem, [here] may be a good place to start). [Cronopio Michele?]

STATISTICS
* Verify tag density and define random benchmarks. [Cronopio Stefano + Ugo]

LEARNING (UNBALANCED)
* Transform dataset into ML-friendly format. [Cronopio All]
* Select library of use (Scikit-learn, Keras, TensorFlow, Theano, etc...). [Cronopio All]
* Compute tagging with unbalanced training dataset with model of choice and compare to random and quasi-random benchmarks (just for fun + get an idea of computation time). [Cronopio All]

AUGMENTATION
* Select subset of categories (tags) that correspond to less than n images. [Cronopio Federico and John?]
* Augment under-represente categories to match n using small angles rotations, translations and zoom (keeping in mind that computation time probably grows linearly with dataset size). [Cronopio Federico and John?]
* Crop whales' tail from background if possible. [TBD]
* Perform normalization check. [TBD]

LEARNING (BALANCED)
* Compute tagging with balanced trainig dataset using a number of models (CNN, Random Forests, Gradient Boost, etc...). [Cronopio All]
* Perform parameter exploration on a selected model. [TBD]
* If computation too heavy, consider moving to server or GPU. [Cronopio Michele and Ugo]
* Select best/combinations of best models. [Cronopio All]

SUBMISSION
* Normalize test set using same procedure as training. [TBD]
* Compute tagging. [TBD]
* Format file for submission (and pray we got accuracy > frequency of most frequent tag). [TBD]
* Repeat (we can submit 5 times per day, best one matters in the end).

## Raw data
The raw data may be recovered on the dedicated [Kaggle page].

## Info
* To all Cronopios: feel free to modify this README as much as you wish.
* During development, it would probably be easier to share kernels generated straight from Kaggle (which include a 18 GB virtual RAM). We will upload code on GitHub once the competition will close.
      
## Useful links
* http://www.subsubroutine.com/sub-subroutine/2016/9/30/cats-and-dogs-and-convolutional-neural-networks
* https://medium.com/nanonets/how-to-use-deep-learning-when-you-have-limited-data-part-2-data-augmentation-c26971dc8ced
* http://neuralnetworksanddeeplearning.com/
* https://machinelearningmastery.com/how-to-develop-a-word-level-neural-language-model-in-keras/
* https://chsasank.github.io/keras-tutorial.html
* https://blog.deepsense.ai/deep-learning-right-whale-recognition-kaggle/
* https://towardsdatascience.com/object-detection-with-neural-networks-a4e2c46b4491
* https://www.kaggle.com/c/whale-categorization-playground
* https://becominghuman.ai/image-data-pre-processing-for-neural-networks-498289068258
* http://cs231n.github.io/convolutional-networks/


[here]: https://towardsdatascience.com/object-detection-with-neural-networks-a4e2c46b4491
[whale sightings]: https://www.kaggle.com/c/whale-categorization-playground
[kaggle page]: https://www.kaggle.com/c/whale-categorization-playground/data

