# Alpha Recognition

This project implements a machine learning model for recognizing alphabets using computer vision techniques. It uses logistic regression to classify handwritten letters captured through a webcam.

## Features

- Loads pre-processed image data and labels
- Trains a logistic regression model on the dataset
- Performs real-time alphabet recognition using a webcam feed
- Displays the predicted letter in real-time

## Dependencies

- numpy
- opencv-python (cv2)
- pandas
- scikit-learn
- Pillow (PIL)

## Setup

1. Ensure you have all the required dependencies installed:

   ```
   pip install numpy opencv-python pandas scikit-learn Pillow
   ```

2. Place your dataset files in the `data` directory:
   - `image.npz`: Contains the image data
   - `labels.csv`: Contains the corresponding labels

## Usage

Run the script `alpha_recognition.py`:

```
python alpha_recognition.py
```

The script will:
1. Load and preprocess the data
2. Train a logistic regression model
3. Open a webcam feed
4. Continuously capture and process frames to recognize alphabets
5. Display the predicted letter in real-time

Press 'q' to quit the application.

## How it works

1. The script loads pre-processed image data and labels.
2. It splits the data into training and testing sets.
3. A logistic regression model is trained on the scaled image data.
4. The webcam feed is processed in real-time:
   - Frames are converted to grayscale
   - A region of interest (ROI) is extracted
   - The ROI is preprocessed to match the training data format
   - The preprocessed image is fed into the model for prediction
5. The predicted letter is printed to the console

## Notes

- The script uses SSL context modification to handle HTTPS verification issues.
- Error handling is implemented to manage potential exceptions during webcam processing.

## Future Improvements

- Implement a graphical user interface for better interaction
- Add support for saving and loading trained models
- Enhance preprocessing techniques for better accuracy
- Expand the dataset to include more diverse handwriting samples
