## Eyepatch: Prototyping Camera-based Interaction through Examples

#### Authors: Dan Maynes, Takeo Igarashi
#### ACM UIST 2007, Rhode Island, USA
#### Computer vision, image processing, classification, interaction

#### Strength
The paper introduces eyepatch, a tool for designing camera-based interactions without needing to have 
in-depth knowledge on specialised CV techniques. One of the strengths of the paper was the use of iterative 
prototyping and the ability to let users combine weak classifiers into one, for effective results. 
Another good thing is that it introduces some of the primary CV classifiers to new comers.


#### Weakness
One of the weakness of the paper was the fact that it was tested only on a small group of computer science graduate students. 
Though the authors gained valuable insight from this, their sample pool of participants was not diverse enough to cover 
other non-technical aspects of the tool(from the perspective of designers or artists).


#### Critique
It is necessary to have the ability to adjust classifier thresholds to a level that is appropriate for different 
applications(fire detector vs free-food detector). Also, it is important to support temporal filtering 
to preserve object coherence across frames and have smooth detected motion paths instead of just assuming the same position 
for object as in previous frames.

Eyepatch has two basic modes:
- Training Mode: where users can train different types of classifiers to recognize the object, region, or parameter that they are interested in
- Composition Mode: where the classifiers are composed in various ways and users specify where the output of the classifiers should go

Classifiers supported in Eyepatch:
- Color: Based on hue histograms and backprojection for identifying distinctively colored objects
- Brightness: for finding the brightest or darkest regions of an image, such as laser dots or shadows
- Shape: based on Canny edge detection followed by contour matching using pair-wise geometrical histograms, for finding objects with distinctive outer contours
- Adaboost: a machine learning technique that uses a boosted cascade of simple features for recognizing general classes of objects like faces, animals, cars, or buildings
- Scale-Invariant Feature Transforms: for recognizing specific objects with invariance to scale, pose, and illumination
- Motion: based on segmentation of a motion history image, for identifying the directions of moving objects in the scene
- Gesture recognition: based on blob detection followed by motion trajectory matching using the Condensation algorithm, for recognizing particular patterns of motion


What did authors learn:
- Provide image data in addition to classifier output
- Allow data selection and filtering.
- Provide a mechanism for data reduction
- Allow users to combine multiple classifiers of the same type into a single classifier that recognizes multiple objects
- Provide the ability to adjust classifier thresholds
- Support temporal filtering for object coherence across frames
- Allow direct manipulation of the classifier model
- Provide a plug-in architecture

Relevant work:
- based on the future work proposed by authors of Crayons(design tool for camera-based interaction), such as supporting additional feature types and taking motion into account.
- authors drew inspiration from Exemplar: viewing the state of the created model, and adjusting it for better results, is very similar to the approach they adopted in Eyepatch
- Papier-Mâché toolkit: provided a high-level programming abstraction that allowed users to extract certain events from a camera input without worrying about the underlying details of the computer vision algorithms
- Authors adopted a dataflow model, and motion classifiers in Eyepatch which is similar to that in Cambience system. Cambience system allowes users to select regions of a video frame in which they wanted to detect motion, and then map the motion in each region to a different sound effect. But Cambience focused on only one type of input (motion) and one type of output (ambient soundscapes).
- Lego Mindstorms's "Vision Command” Kit: was one of the first systems to attempt to make computer vision accessible to novice programmers Its visual programming interface allowed users to test for simple conditions in a camera image: when a certain color or a certain brightness threshold was seen in one of five regions of the frame, an event could be triggered.


