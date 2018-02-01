## Matrix: A realtime object identification and registration method for augmented reality

#### Authors: Jun Rekimoto
#### CHI 1998, Japan
#### Keywords: Augmented reality, Cameras, Magnetic sensors, Sensor systems, Image recognition, Registers, Position measurement, Volume measurement, Ultrasonic variables measurement, Magnetic devices

#### Strength
I like the authoring tool that allowed system developers to register annotation information with real world objects instead of manually calculating them. Determining the position of a three-dimensional point in the real world based on the stereo vision method is a good idea and avoid complex manual calculations in three-dimensional space. 

- allow users to view real world objects with spatially registered digital annotation.
- information authoring tool

#### Weakness
- Authors did not explain why they only used their own internal data format and not any of the standardized three-dimensional graphics format such as VRML or DXF. It was not clear whether the internal three-dimensional data format simply served as a representation of the data points, or brought any performance benefits over standard formats.


#### Future Work
Other than simply projecting static models over the markers, I would like to extend this project by overlaying information in the form of "motion graphics" in three dimentional space to illustrate a concept. This would be useful in explaning phenomenons/events that involve multiple steps.

---

**System description**
Authors proposed a new technique for producing augmented reality systems that simultaneously identify real world objects and estimate their coordinate systems.
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
- Bajura and Neumann used LEDs as landmarks and demonstrated vision-based registration for AR systems.
- Uenohara and Kanade used template matching for object registration. 
- State et al. proposed a hybrid method of combining landmark tracking and magnetic tracking (they used color markers as landmarks).
