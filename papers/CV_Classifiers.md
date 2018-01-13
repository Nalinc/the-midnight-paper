## Computer Vision Classifiers:

**Boosted cascade of Haar classifiers:** for identifying objects of a general class, such as cars or faces
**SIFT classifier(Scale-invariant feature transform):** for identifying a particular instance of a class, such as a specific book cover or logo.

But neither of these feature-based classifiers performs well when attempting to identify smooth, untextured objects like 
balloons or laser dots, since they have few distinguishable features; in this case a classifier based on hue histograms or 
brightness thresholding is more appropriate.

**frame differencing, motion templates, adaptive background subtraction, or optical flow:** Techniques for capturing change in the image over time(when following a moving object)

**color classifier:** for extracting skin-colored regions
**motion classifier:** that identifies moving regions of the image

^by combining these two, we can detect "moving", "skin-colored" regions.

Classifiers supported in Eyepatch:
- Color: Based on hue histograms and backprojection for identifying distinctively colored objects
- Brightness: for finding the brightest or darkest regions of an image, such as laser dots or shadows
- Shape: based on Canny edge detection followed by contour matching using pair-wise geometrical histograms, for finding objects with distinctive outer contours
- Adaboost: a machine learning technique that uses a boosted cascade of simple features for recognizing general classes of objects like faces, animals, cars, or buildings
- Scale-Invariant Feature Transforms: for recognizing specific objects with invariance to scale, pose, and illumination
- Motion: based on segmentation of a motion history image, for identifying the directions of moving objects in the scene
- Gesture recognition: based on blob detection followed by motion trajectory matching using the Condensation algorithm, for recognizing particular patterns of motion







