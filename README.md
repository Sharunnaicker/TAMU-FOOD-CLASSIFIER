# A&M AI/ML FOOD CLASSIFIER
## [Srilokh Karuturi](https://www.linkedin.com/in/srilokh-karuturi/)
## [Sharun Naiker](https://www.linkedin.com/in/sharun-naicker-17954a1a4/)
## [Nehanth Narendrula](https://www.linkedin.com/in/nehanth-narendrula-693a2b192/)
## [Austin Hale](https://www.linkedin.com/in/austin-hale-53940622b/)
###### A&M HACK JAN 2022

![github](https://myoctocat.com/assets/images/base-octocat.svg)
![logo](https://raw.githubusercontent.com/Nehanth/TAMU-FOOD-CLASSIFIER/a41feb07e76367070111845f971781b1e0d86598/App/Assets.xcassets/AppIcon.appiconset/Group%201-1.svg)

## We have created an `IOS application` that will utilize `AI/ML` to determine the exact food `via a photo`.

> Features
- [x] #1
- [x] The program will be able to upload/take photos for analysis.
- [x] Create ML Model using CreateML
- [x] IOS APP Integegration with ML Model

> Requirements
- [x] Upload/Take Photo for Analysis
  - [x] Get permission from apple device for camera access/library access.
  - [x] When the user presses the screen with one touch, use the camera for a photo 
  - [x] When the user presses screen with two touches, access the photo library for upload 
- [x] Create ML Model using CreateML
  - [x] Download Data Set from Kaggle of gigabytes of photos for food
  - [x] Use CreateML
   - [x] Upload all photos and set specific augmentations (crop, rotation, blur, exposure, noise, flip)
   - [x] Train Model
   - [x] Analyze to check accuracy with specific test cases and retrain if needed
   - [x] Extract the ML Model
   - [x] Implement ML Model into our IOS Swift Application    
- [x] Implement ML Model
 - [x] Move ML Model Into Model’s Folder with name “imagetest.mlmodel” 
 - [x] Implement ML MOdel into ImagePredidictor.swift


> Software Documentation 

App:
 - Assets.xcassets/AppIcon.appiconset -  visuals/dimensions for the app logo
 - /Base.lproj - visual representation of the user interface of an iOS application
 - AppDelegate.swift - Manages shared application data
 - Info.plist - supply crucial information in dictionary form (key, value)

Configuration:
 - SampleCode.xcconfig - allows for different build settings
 
Extensions:
 - CGImagePropertyOrientation+UIImageOrientation.swift - Switch statement for managing image orientation
 - VNClassificationObservation+confidenceString.swift - Function using a switch statement to output percentage confidence of ML
 - imagetest.mlmodel - ML model

Image Predictor:
 - ImagePredictor.swift - Class for interacting with the MLmodel to create a prediction
    - Struct for storing prediction outcome
    - Function for creating a request to coreML for a classification
    - Function for making a prediction using ML
    - Vision request handler function

Main View:
 - MainViewController+CameraPicker.swift - utility to take a photo with camera
 - MainViewController+PhotoPicker.swift - utility to use library
 - MainViewController.swift - utility for single and double tap
 - Base.lproj - visual representation of the user interface of an IOS

Models:
 - LICENSE.txt - Legal documentation
 - NOTICE.txt - Documentation for Authors, link, and license
 
TAMU FOOD CLASSIFIER.xcodeproj: .xcode file (on runtime)
