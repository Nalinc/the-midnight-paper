## The Office of the Future : A Unified Approach to Image-Based Modeling and Spatially Immersive Displays

#### Authors: Ramesh Raskar, Greg Welch, Matt Cutts, Adam Lake, Lev Stesin
#### Conference: SIGGRAPH 1998
#### Keywords: Display, spatially immersive display, intensity blending, image-based modeling, image-based rendering, range, depth, reflectance, projection, virtual environments, calibration, autocalibration.

#### Strength
I like the way how authors calibrated their system with multiple devices for depth extraction. They first calculated the intrinsic and extrinsic parameters of the camera using a checkerboard pattern on a flat surface. Then, they used the same technique to calibrate the projector. Combining the transformation parameters from both was a clever way to tackle the calibration problem.

#### Weakness
Authors used camera image differencing to detect the changes in the scene geometry. This technique is not only prone to give false positives due to drifts in calibrating the cameras, but might not work at all if display surfaces lack texture.

#### Future Work
Spatially immersive display surfaces can be used to render graphics that resemble the weather outside one's house. This would not only simulate a natural environment right inside the house, but also update users to be prepared before they leave the room.
