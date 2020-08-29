# Rock-Paper-Scissors-Lizard-Spock-App

This is a simple web page that uses transfer learning in Tensorflow.js to learn to distingish between 6 hand positions relating to the Game Rock, Paper, Scissors, Lizard, Spoc 

1.No gesture

2.Rock gesture displayed

3.Paper gesture displayed

4.Scissors gesture displayed

5.Lizard gesture displayed

6.Spoc gesture displayed

The App allows you to present an image of a hand (via your webcam) and select the gesture displayed. Each seperate image presented helps the app to learn the gesture.

As the app learns, it will attempt to categorise newly presented images in real-time to determine the correct guesture.

The more distinct images it learns the more accurate it should be.

# Installing and Running

The app is constructed as a single HTML page and can be run from the local file system in a recent Chrome browser.

This has not been tested across different browsers

The following instructions can be used to clone and run this application on your machine:

1. Clone the repo from Git git clone https://github.com/sajid-619/Rock-Paper-Scissors-Lizard-Spock-App.git

2. Open the index.html file in a Chrome browser

3. Allow the page to access your WebCam

4. Using your WebCam train the app to recognise you showing no gesture, Rock, Paper, Scissors, Lizard and Spoc gesture (at least 1 for each category but more is better)

5. Once the app has learned a single category it begins to predict the gesture shown. If it is getting a particular class wrong, then train more instanceof that class.

# How it works

The application takes image frames from the webcam and uses transfer learning (MobileNet) to capture the activations for the image. Each image of a guesture is classified as one of the 5 game gestures along with a no gesture image and thae activations for these are stored in a KNN Classifer.

When a new image frame is presented, the image is passed through the MobileNet classifier to obtain the activations; these are then passed to the KNN Classifier which attempts to find the closest classification based on the captured gestures.


# Ability to switch cameras
Currently this uses the default camera but it would be nice to be able to swap cameras
Add feature to play the game
Maybe learn the game via RL (e.g. DDPG) and play
