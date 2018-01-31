## Matrix: A realtime object identification and registration method for augmented reality

#### Authors: Jun Rekimoto
#### CHI 1998, Japan
#### Keywords: Augmented reality, Cameras, Magnetic sensors, Sensor systems, Image recognition, Registers, Position measurement, Volume measurement, Ultrasonic variables measurement, Magnetic devices

#### Strength
I like the way authors created a separate tool that allowed developers to register annotation information with real world objects. This authoring tool determine the position of a 3D point in the real world based on the stereo vision method.

- allow users to view real world objects with spatially registered digital annotation.
- information authoring tool

#### Weakness

#### Future Work

---

**System description**
- With the hand-held configuration, the user holds a hand-held device consisting of a palmtop display and a video camera, which provides a computer augmented view of the real world (i.e., video see-through). 
- With the head-mounted configuration, the user wears the Sony GlassTron head-mounted display, with a miniature video camera (the user sees the real world as the video images).
- When the system identifies a real world object from the attached code, the corresponding 3D overlay information is retrieved from the database. 
- Using the estimated camera position, this information can correctly be superimposed on the video image.

**Camera position and pose estimation:**
- From 4 known coplanar (real world) points on the image plane, it is possible to calculate a matrix representing the translation and rotation of the camera at a real-world coordinate. 
- They used 4 corners of the 2D-code frame as these reference points

**point estimation on 3d plane**
- The user first prepares two still images of the target object (both come with the same attached 2D matrix code in the view). 
- Then the user clicks on the two corresponding points on the two images. 
- The system recognizes the 3D coordinate systems of both of the images by using the 2D matrix, and determines the 3D
position based on the pair-of 2D points.



**Hardware:**
- head-mounted and hand-held augmented reality systems running on the SGI O2 workstation
- average screen update rate was from about 15 Hz to 30 Hz (depending on the complexity of displaying information)


**Relevant work:**
-
