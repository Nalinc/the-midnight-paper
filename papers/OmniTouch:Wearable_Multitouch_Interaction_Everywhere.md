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

#### Extension
I would extend OmniTouch to explore typing techniques on projected virtual keyboards. What are users' preferences for different typing surfaces, how to tackle occlusions on them and different ways to provide haptic feedback on such surfaces.

---
**Hardware specifications:**
- First is a custom, short-range PrimeSense depth camera, which pro- vides a 320x240 depth map at 30 FPS. Objects as close as 20cm can be imaged by this sensor, with relative error in the depth (Z) axis of approximately 5mm.
- The second key component is a Microvision ShowWX+ laser pico-projector. This projector has the important property of wide angle, focus-free projection of graphical elements regardless of depth
- Both the depth camera and projector are rigidly mounted to a form-fitting metal frame, which is worn on the shoulders, and secured with a chest strap. Camera and projector are tethered to a desktop computer for prototyping purposes


**What did authors learn:**
- 

**Relevant work:**
- SixthSense and Interactive Dirt both featured a worn cam- era/projector combination.
- Skinput uses bio-acoustics to detect finger tap events on the skin. But it does not support for any surface other than the user’s body, do not detect touch drag movements, and the lack of support for multitouch.

