## Surround-See: Enabling Peripheral Vision on Smartphones during Active Use

#### Authors: Xing-Dong Yang, Khalad Hasan, Neil Bruce, Pourang Irani
#### UIST 2013 St Andrews, United Kingdom
#### Peripheral mobile vision, mobile ‘seeing’, mobile surround vision.

#### Strengths
Surround See gives mobile device the ability to perceive specific objects in its periphery and allow the user to trigger certain actions by pointing at them. This not only enable devices to be aware of their surroundings but also augment user interaction with the device itself. Such user and situation awareness in devices has the potential to shape the design of future products in market. Some other strengths are
- Allows users to point at objects in the environment to interact with content
- Let users operate(pointing/waving) the mobile device at a physical distance even when the user is not holding it.
- Can trigger reminders based on an environment it recognizes.
- It can perceive specific objects in the mobile device’s periphery (i.e. speakers), which the user can control by pointing at them. 
- Surround-See can identify when the user walks away from it
- Use phone's built-in compass to fix issues with ORB in different orientations. 
  - This is done by loading a list of reference images and their corresponding orientations in the begining, and using them to rotate the input frames during the recognition process.

#### Weakness
- Authors did not explain how to handle false positive gestures. Situations where someone accidentally waves a hand from a peripheral distance while the real user is near the phone are not addressed. This essentially means that at some point, both front-camera and omni-vision camera need to detect faces simultaneously which would introduce latency and delay appropriate action that needs to be taken
- Under 'Recognizing hand postures', authors mentions that '1' posture, with the index finger is reserved for pointing. However, under 'Posture for Speed-dialing', they talk about mapping 5 phone numbers to the 5 hand postures (from 1 to 5). They dont really clarify how Surround-See distuinghes between 'pointing' and 'speed-dialing 1' gesture.

#### Future Work
- I would extend Surround See's ability to perceive its environment by integrating a classifier that auto-detects the type of room where device is being used and adjust necessary settings accordingly(sound, airplane mode). It would be similar to how most of the present day devices have auto-brightness setting. Such a classifier can cover common places like airport, lecture hall, bedroom or outdoors.

---
**System Description**
- Surround-see brings the the concept of enabling mobile devices to ‘see’ their surroundings. It is a self-contained smartphone equipped with an omni-directional camera that enables peripheral vision around the device to augment daily mobile tasks.

**Surround see capabilities**
- Recognizing the Device’s Peripheral Environment
  - This was implemented using Local Binary Patterns (LBP) and a machine learning classifier. Before the recognition process, they pre-processed the raw omni-directional image by un-wrapping it to a panoramic image using the method described in. Then **they used LBP to describe the image using a unique feature vector**(histogram of the microstructures). LBP detects microstructures inside an image (e.g. lines, edges) and is orientation and luminance invariant. The feature vector was used to train a machine learning classifier or to recognize a peripheral environment. To train the classifier, they used Chang and Lin’s LIBSVM library using the Support Vector Machine (SVM). They used a RBF Kernel with parameters that gave the highest 5-fold cross-validation scores
  - Recognizing an Object in the Smartphone’s Environment
    - An **object in the device’s environment is recognized using feature point matching using the ORB algorithm(Oriented FAST and Rotated BRIEF)**. ORB searches each input frame for a desired object using a reference image.
    - ORB suffers from orientatons related issues. Surround See fixes this by loading a list of reference images and their corresponding orientations in the begining, and using them to rotate the input frames during the recognition process.
  - Recognizing the User’s Hand(Skin Detection)
    - Surround-See **detects the user’s hand using a skin color model in YCbCr color space**. A skin color pixel was detected if its Cr and Cb values fall into the ranges [140, 166] and [135, 180] respectively.
    - The user’s hand was detected by looking for blobs that are larger than a threshold size.
    - This is error prone when the background contains colors close to that of the user’s skin. 
    - So they dynamically filtered out the background noise by removing the blobs that appeared in the same location for a certain fixed number of frames (e.g. 30 in Surround See).
  - Tracking fingertips
    - Upon extracting the user’s hand contour, the user’s fingertips were detected by searching through the contour points, and identifying those with a curvature less than a threshold value (e.g. 50˚)
    - It can detect the finger’s up-and-down (vertical) motion by calculating the distance from the detected fingertip to the center of the omni-directional image, where an increase in the distance indicates that the finger is moving upward, and a decrease means the opposite.
  - Recognizing hand postures: A hand posture is recognized by counting the number of detected fingertips.
  - Detecting pinching: **Pinch is detected using Wilson’s method**, where a pinch is recognized when there is a connected blob inside a hand contour Pinch can be used as a ‘mouse click’ to confirm an action or to trigger a command.
- Detecting User Activities in the Periphery
  - **They used optical flow for Motion Detection** to determine device's proximity to the user. Spreading of the motion vectors indicated that Surround-See was being placed closer to the user and the gathering of the motion vectors indicated that Surround-See was being moved away from the user.
  - Remote gesturing: assumes the phone is sitting on a stable platform such as a table and that the view is uncluttered. This allows them to use background subtraction to remove any skin-color noise in the background.
  - detect user’s activity within a user-defined region of interest (ROI) (eg. someone enters from door)

**Surround See interactions**
- Pen vs. Touch Input
- Off-screen Pointing
- Controlling Remote Objects (Physical Shortcut)
- Posture for Speed-dialing
- Location-based Messaging
- Proximity-based Screen Rotation
- Notify to Take the Phone

**Hardware Specification:**
- The prototype is a HTC Butterfly smartphone with an omni-directional lens from Kogeto mounted on its front-facing camera.
- The omni-directional lens has a 360˚ and 56˚ field-of-view in the horizontal and vertical planes, respectively.
- The smartphone was running on the Android operating system on a Quad-core 1.5 GHz Krait CPU with 2GB of RAM.
- The front camera had a maximum resolution of 2MP. For realtime image processing, they down-sampled the resolution to 960×720. 

**Relevant work:**
- Hinckley et al.’s seminal work on sensing techniques for mobile interaction opened a new wave of interfaces that exploit a mobile device’s state, such as its orientation.
- Byung et al presented one-handed approach to control virtual objects(AR) on a mobile screen,
- Hinckley et al proposed sensing techniques for mobile interaction(like automatically reorienting images)
- Gasimov et al proposed a framework for effective context-aware mobile web browsing to support navigation in applications.
- Eleanor Jones et al investigated different gesture based interactions and how to enter text with devices that are solely enabled with accelerometers.
- Schmidt et al. augmented mobile devices with tilt, light and heat sensors to identify if the device is resting on a table, is in a pocket, or is being used outside.
- SideSight and HoverFlow made single finger interaction around the device possible by using IR distance sensors to capture gesture-based interactions above and to the sides of the device.
- Abracadabra facilitates input by activating states of a magnetic sensor and maps these to menu and cursor control
