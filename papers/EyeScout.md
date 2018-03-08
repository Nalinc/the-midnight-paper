## EyeScout: Active Eye Tracking for Position and Movement Independent Gaze Interaction with Large Public Displays

#### Authors: Mohamed Khamis, Axel Hoesl, Alexander Klimczak, Martin Reiss, Florian Alt, Andreas Bulling
#### UIST 2017, Quebec City, QC, Canada
#### Keywords: Gaze Estimation; Body Tracking; Gaze-enabled Displays

#### Strength
I like the way paper describes different modalities in gaze interaction. While most of the previous work is focused on  "Walk then Interact", EyeScout also focuses on "Walk and Interact" by detecting gaze without needing to calibrate the eye tracker for each user. This reduces gaze interaction kickoff time and makes EyeScout faster than other state-of-the-art methods.

The way authors have described horizontal flexibility of public displays from "Sweet Spot" to "Sweet Line", 

#### Weakness
Although EyeScout has extended horizontal flexibility of public displays from "Sweet Spot" to "Sweet Line", 
their vertical flexibility is still limited to a narrow range of angle between eye-tracker and head. This angle 
depends on user's height and his distance from the tracker, and therefore limits the close-distance interactions in EyeScout. 

#### Future Work
I would like to extend EyeScout's vertical flexibility. This can be done by either allowing the camera to move on a vertical line, 
or tilting it on the vertical axis. Such vertical flexibility can be leveraged in games which require users to jump without losing the gaze.

