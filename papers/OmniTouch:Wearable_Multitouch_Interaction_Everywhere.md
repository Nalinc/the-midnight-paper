## OmniTouch: Wearable Multitouch Interaction Everywhere

#### Authors: Chris Harrison, Hrvoje Benko, Andrew D. Wilson
#### UIST 2011, Santa Barbara, CA, USA
#### On-demand interfaces, finger tracking, on-body computing, appropriated surfaces, object classification 

#### Strength
Use of flood-fill heuristic instead of using only z-distance for finger click detection is intriguing. Their flood-fill technique not only detects finger clicks robustly, but also maintains it when dragging a finger across irregular organic surfaces.

- It was interesting to see the use of flood-fill heuristic instead of z-distance for finger click detection. Their algorithm first compute the midpoint of the finger path, which roughly equates to the location of the minor knuckle. From this point, they flood fill towards the fingertip using a tolerance of 13mm in depth map to determine if neighboring pixels can be filled. Simple hovering flood fills the entire finger, whereas in physical touch, the fill operation floods out into the connecting object.
- I like the way they lock a surface once it is identified and the interface is placed, and how they track the surface change frame-to-frame and accordingly adjust the interface to reflect this change.

#### Weakness
It is not clear if we can use such camera and projector based interaction for outdoors, or at places where natural light is way brighter than what a projector can project on a surface. Besides, authors only explored short term user-interactions with projected interfaces which only serve as a proof-of-concept but does not give much insight on whether they are actually engaging or not.

#### Future Work
- I would extend OmniTouch to explore typing techniques on projected virtual keyboards. What are users' preferences for different typing surfaces, how to tackle occlusions on them and different ways to provide haptic feedback on such surfaces.
- It is possible to create 3D meshes of objects, allowing for distortion free projection onto non-planar surfaces (i.e., projective texturing). 
- Additionally, postures and gestures of the arms and hands could be used for input. For example, a "telephone" gesture with hands could summon a keypad on the arm, while a “back of hand” pose could render a watch on the wrist.

---
**Hardware specifications:**
- First is a custom, short-range PrimeSense depth camera, which pro- vides a 320x240 depth map at 30 FPS. Objects as close as 20cm can be imaged by this sensor, with relative error in the depth (Z) axis of approximately 5mm.
- The second key component is a Microvision ShowWX+ laser pico-projector. This projector has the important property of wide angle, focus-free projection of graphical elements regardless of depth
- Both the depth camera and projector are rigidly mounted to a form-fitting metal frame, which is worn on the shoulders, and secured with a chest strap. Camera and projector are tethered to a desktop computer for prototyping purposes


**System description**
* OmniTouch can use a surface’s lock point and orientation to provide an interface that tracks with a surface. It has three distinct approaches to define, present, and track interactive areas
  - One Size Fits All: the interface can only be as big as the smallest conceivable surface (generally the hand)
  - Classification-Driven Placement: In this, the system first differentiates between a small set of surfaces by performing surface classification. Second, the system automatically sizes, positions and tracks an interface given the available projection area and heuristics describing the appropriate location for that surface. (suffers from scalability issues, since it is simply not possible to build a classifier for every conceivable surface)
  - User-Specified Placement: let the user define the interactive area. They can either "click" on a surface, causing a generically sized interface to be centered at that location, or a user can click and drag to position and size in one continuous action.

**Relevant work:**
- SixthSense and Interactive Dirt both featured a worn camera/projector combination.
- Skinput uses bio-acoustics to detect finger tap events on the skin. But it does not support for any surface other than the user’s body, do not detect touch drag movements, and the lack of support for multitouch.
- LightSpace uses an array of depth cameras to track users and arm-level manipulations in an augmented room.

**Evaluation:**
Researchers recruited 12 participants from their local metropolitan area for one hour sessions and compared their method to the gold standard - capacitive touch screens - drawing performance results from the literature. 
