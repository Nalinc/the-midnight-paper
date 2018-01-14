## Robust Computer Vision-Based Detection of Pinching for One and Two-Handed Gesture Input

#### Authors: Andrew D Wilson
#### UIST 2006, Montreux, Switzerland
#### gesture, computer vision, bimanual interaction, hand tracking

#### Strength
Interesting use of connected components of the segmented background against the hand to detect pinch gesture. By detecting the hole formed when the thumb touches the forefinger, this technique avoids the use of complex hand shape analysis, sophisticated pattern recognition techniques and fingertip tracking to detect pinch gesture.

#### Weakness
The technique assumes a camera will be mounted on top of a keyboard to detect gestures. Though this setup makes background static, it is quite uncommon and not much convenient for general use. While paper defines hole components as those background components of significant size that have no pixels on the border, it does not explain if this can be generalized across different hand colors/sizes.
- The detection of the hole formed by the thumb and forefinger depends on the quality of the segmentation(which is difficult in uncontrolled viewing circumstances or mobile scenarios).
- The technique depends on the formation of a hole between the thumb and forefinger, through which the background is visible(no hole is formed if the user curls the other fingers underneath the thumb and forefinger)
- When used as a hand-tracker, the pinch detector may be limited by the fact that the tracked position corre- sponds to the center of the hole component, not the position of the point where the thumb and forefinger touch
- The technique does not support both tracking and dragging without an extra transition.
- Single hand and bimanual interaction techniques are not coherent in TAFFI(for example zooming by moving hand up/down above the surface in single mode vs pulling two pinched hands apart in bimanual; panning by pinching and moving hand across surface in single hand mode vs moving both hands in the same direction in bimanual)
- The technique assumes a camera will be mounted on top of a keyboard to detect gestures. Though this setup makes the background static, it is quite uncommon and not so convenient in general use.

#### Critique
I would extend this pinch detection technique to non-static backgrounds with semi/un-controlled viewing circumstances. This technique should further be applied to create coherent interactions which stays consistent across different user preferences(one/two handed inputs). For example, single hand and bimanual interaction techniques are not coherent in TAFFI prototype but this can be fixed.

---

**Usefulness of pinch gesture**
- It is evocative of grabbing or picking up an object, and so offers a natural signal to select or move an object in an interactive system.
- The pinching grasp is precise and stable. The hand is able to bring the thumb and forefinger together and apart quickly.
- From the user’s point of view there is little am- biguity whether the thumb and forefinger are touching. other poses (such as the extended index finger) are inherently ambiguous by comparison.
- Pinch gestures are relatively easy to detect if the sensing technology provides detailed information on the configuration of the hand, or when contacts are embedded in the fingertips of a glove.

In Graph Theory, there exists a path between any two vertices of a "connected component". In image processing, such components refer to connected groups of identically labeled pixels in a binary image; often each component corresponds to a distinct object which is subsequently analyzed

*In CV, image segmentation is the process of partitioning a digital image into multiple segments (sets of pixels, also known as super-pixels). The goal of segmentation is to simplify and/or change the representation of an image into something that is more meaningful and easier to analyze. Image segmentation is typically used to locate objects and boundaries (lines, curves, etc.) in images*

**The pinch detection algorithm:**
- Obtain a binary segmentation of the hand and back- ground
- Compute connected components of the background pixels from the binary image. Label each border pixel with the component that contains it.
- Take components of significant size (in number of pix- els) that do not have pixels on the border of the image. Each of these is a ‘hole’ indicating a pinching hand.


**Relevant work:**
-
