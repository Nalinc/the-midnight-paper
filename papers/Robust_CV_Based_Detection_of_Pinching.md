## Robust Computer Vision-Based Detection of Pinching for One and Two-Handed Gesture Input

#### Authors: Andrew D Wilson
#### UIST 2006, Montreux, Switzerland
#### gesture, computer vision, bimanual interaction, hand tracking

#### Strength
Using connected components of the background segmented against the hand to detect the hole that is formed while making a pinch gesture is amazing. This technique avoids the use of complex hand shape analysis, sophisticated pattern recognition techniques and fingertip tracking to detect pinch gesture.

recover position and shape of hands. 

While most of the previous techniques to detect pinch gesture were based on precise hand shape analysis or fingertip tracking, this technique 

This technique avoids the use of complex detection and tracking methods with sophisticated pattern recognition techniques to recover the position and shape of the hands.

While most approaches use a standard detection and tracking paradigm with sophisticated pattern recognition techniques to recover the position and shape of the hands, 

#### Weakness
- The detection of the hole formed by the thumb and forefinger depends on the quality of the segmentation(which is difficult in uncontrolled viewing circumstances or mobile scenarios).
- The technique depends on the formation of a hole between the thumb and forefinger, through which the background is visible(no hole is formed if the user curls the other fingers underneath the thumb and forefinger)
- When used as a hand-tracker, the pinch detector may be limited by the fact that the tracked position corre- sponds to the center of the hole component, not the position of the point where the thumb and forefinger touch
- The technique does not support both tracking and dragging without an extra transition


#### Critique

---

** Usefulness of pinch gesture**
- It is evocative of grabbing or picking up an object, and so offers a natural signal to select or move an object in an interactive system.
- The pinching grasp is precise and stable. The hand is able to bring the thumb and forefinger together and apart quickly.
- From the user’s point of view there is little am- biguity whether the thumb and forefinger are touching. other poses (such as the extended index finger) are inherently ambiguous by comparison.
- Pinch gestures are relatively easy to detect if the sensing technology provides detailed information on the configuration of the hand, or when contacts are embedded in the fingertips of a glove.


**The pinch detection algorithm:**
- Obtain a binary segmentation of the hand and back- ground
- Compute connected components of the background pixels from the binary image. Label each border pixel with the component that contains it.
- Take components of significant size (in number of pix- els) that do not have pixels on the border of the image. Each of these is a ‘hole’ indicating a pinching hand.


**Relevant work:**
-
