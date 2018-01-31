## Matrix: A realtime object identification and registration method for augmented reality

#### Authors: Jun Rekimoto
#### CHI 1998, Japan
#### Keywords: Augmented reality, Cameras, Magnetic sensors, Sensor systems, Image recognition, Registers, Position measurement, Volume measurement, Ultrasonic variables measurement, Magnetic devices

#### Strength
I like the way authors created a separate tool that allowed developers to determine the position of a 3D point in the real world based on the stereo vision method.

(register annotation information with real world objects)

- allow users to view real world objects with spatially registered digital annotation.
- information authoring tool

#### Weakness

#### Future Work

---

**Camera position and pose estimation:**
- From 4 known coplanar (real world) points on the image plane, it is possible to calculate a matrix representing the translation and rotation of the camera at a
real-world coordinate. 
- They used 4 corners of the 2D-code frame as these reference points

- The user first prepares two still images of the target object (both come with the same attached 2D matrix code in the view). 
- Then the user clicks on the two corresponding points on the two images. 
- The system recognizes the 3D coordinate systems of both of the images by using the 2D matrix, and determines the 3D
position based on the pair-of 2D points.



**Hardware:**
- head-mounted and hand-held augmented reality systems running on the SGI O2 workstation
- average screen update rate was from about 15 Hz to 30 Hz (depending on the complexity of displaying information)


**Relevant work:**
-
