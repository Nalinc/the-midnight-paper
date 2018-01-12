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
