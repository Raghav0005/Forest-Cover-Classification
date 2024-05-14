# Project Overview

This project uses _Tensorflow_, _Sci-kit Learn_, _Pandas_, and _NumPy_ to perform multi-class classification of Forest Covers using a deep feed-forward neural network.
The categories that it is classified into are Spruce/Fir, Lodgepole Pine, Ponderosa Pine, Cottonwood/Willow, Aspen, Douglas-fir, Krummholz.

The provided dataset contains cartographic variables that pertain to different forest cover types. In order to be used for training and prediction, it must be run through a series of pre-processing tasks to make it viable for use by the neural network. Initially, it is split into feature and label datasets, containing raw data, and prediction attributes respectively. Using scikit-learn, each is then split further into training and validation datasets, to train the neural network. 

More specifically, the features were fitted and transformed using the StandardScaler, and the label was only transformed to prevent data leakage.

The Neural Network was created with 3 main layers, with 64, 32, 8 neurons respectively. They used the _relu_ and _softmax_ activation functions.
The epochs and batch_size parameters were tuned further to optimize the CPU/GPU usage with overall model performance.
EarlyStopping was also implemented when fitting the model to ensure it does not overfit.

Finally, the preprocessed data and labels are again loaded for prediction purposes. Finally, a classification report of the results is displayed.
