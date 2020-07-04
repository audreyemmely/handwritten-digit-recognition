# Handwritten Digit Recognition
Web application that can predict the digit you draw on the canvas.

## Installing
Clone this repository to your local computer

```
git clone https://github.com/audreyemmely/handwritten-digit-recognition.git
```

Point your localhost to the cloned root directory

Browse to http://localhost/index.html

## Starting predicting handwritten digit
* Draw on the canvas with your mouse on desktop
* Click "Predict" to get result of the handwritten digit prediction
* Click "Clean" to start drawing again

## Pre-trained model
Use MNIST dataset from Keras with CNN (Convolutional Neural Network)
```python
model = keras.Sequential([
    keras.layers.Conv2D(35, (5, 5), padding="same", input_shape = [28, 28, 1]),
    keras.layers.MaxPool2D((2, 2)),
    keras.layers.Conv2D(64, (5, 5), padding="same"),
    keras.layers.MaxPool2D((2,2)),
    keras.layers.Flatten(),
    keras.layers.Dense(1024, activation='relu'),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(10, activation='softmax')
])

model.compile(optimizer = 'adam', loss = 'categorical_crossentropy', metrics = ['accuracy'])
```
## Library
* [jquery](https://code.jquery.com/jquery-3.3.1.min.js) - JQuery
* [tensorflowjs](https://github.com/tensorflow/tfjs) - JavaScript library for training and deploying machine learning models
* [Chart.js](https://github.com/chartjs/Chart.js) - JavaScript library for display charts
