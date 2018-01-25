## VisionWand: Interaction Techniques for Large Displays using a Passive Wand Tracked in 3D

#### Authors: Xiang Cao, Ravin Balakrishnan
#### UIST 2003 Vancouver, BC, Canada
#### vision tracking, large displays, gestures, interaction techniques, input devices, buttonless input

#### Strength
I like the simplicity in design of VisionWand that leverages different haptic profiles associated with different gestures instead of physical buttons to trigger an action. End users can use the wand as a normal stick and do not need to worry about pressing different buttons while performing a certain task. VisionWand works with easily understandable actions which is great.

#### Weakness
Having different wands for different purposes is analogous to having different remotes and we all know how frustrating it could get eventually. A Thermostat remote cannot be used to control Television because of restrictions that physical buttons impose. VisionWand's simple design does not suffer from such restrictions but having different types of wands can totally break this simplicity.

#### Future Work
I would like to give VisionWand an ability to create custom gestures(spells) to unlock features or make it accessible only for selected wand holders. Such a feature could get even more interesting if the system can also interface with other devices like Television or Thermostat and give restricted access.

---
**Hardware Specifications:**
- A pair of Logitech QuickCam Pro 3000 cameras are used for tracking.
- VisionWand itself is a simple cylindrical piece of plastic with different colored ends. 
- Standard stereo vision techniques are applied to track the wand in 3D.

**Interaction techniques**
An object has three possible states: selected, captured, and unselected. Because there are no buttons to indicate the state of the VisionWand itself, switching between these object states is achieved using the tap gesture.
The blue end of the VisionWand performs the basic manipulations. While pointing at an object with the blue end, a tap gesture captures it. A second tap gesture releases the object (i.e. switches it from captured to selected). A tap gesture in any blank area of the screen deselects all currently selected objects. The scale factor of the object is controlled by the distance between the wand and the screen.

- Pointing posture: point to a position on screen; the end that is nearer to the screen is defined as the active end. 
- Parallel posture: keep the wand approximately parallel to the screen, in any orientation. 
- Tilt gesture: starting from a parallel posture, tilt the wand in either direction. 
- Tap gesture: quickly move the active end away from the screen and back again. 
- Parallel tap gesture: from parallel posture, quickly move the entire wand away from the screen and back again. 
- Flip gesture: quickly flip the wand end to end, keeping the orientation and tilt approximately the same as before the gesture. 
- Push and Pull gestures: change the distance between the wand and the screen. 
- Rotate gesture: change the orientation of the wand while keeping it in a parallel posture

