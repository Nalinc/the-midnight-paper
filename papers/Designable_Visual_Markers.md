## Designable Visual Markers

#### Authors: Enrico Costanza and Jeffrey Huang
#### CHI 2009, Massachusetts, USA
#### Visual marker recognition, visualmarker design,mobile devices, mobile HCI, UI toolkits, fiducial recognition, user studies.

#### Strength
Using connected components to construct the topology of markers and not relying on their geometrical features for marker detection is the biggest strength of this paper. This not only makes the detection process scale and rotation invariant, but also resilient to other types of distortion as long as the topology is not affected.

- enables the creation of markers which are both machine- and human- readable
- allows users to create their own visual markers, controlling their aesthetic qualities and what they visually communicate to others.
- recognition is based on topological features of themarkers rather than their geometry.
- d-touch markers are scale and rotation invariant. They are even resilient to other types of distortion such as stretching, as long as their topology is not affected.


#### Weakness
Markers and IDs are application-specific. One of the reasons why bar-codes and QR codes became so popular is because they are consistent and globally distinguishable. Having different applications maintaining their own database of d-touch markers will restrict its use to a limited audience.

- Markers and IDs to be application- specific, rather than having one central repository. One of the reasons why barcodes and QR codes bacame popular is because they were universally distinguishable. Having different applications maintaining their own database of d-touch markers will restrict it use to a limited audience.
- The relatively small size of the IDaddress space (compared to 2D barcodes) implies that markers cannot encode URLs directly.
- Some objects with similar connected-components profile will end up getting same IDs and number of distinct IDs that can be supported by the system is relatively less.

#### Future Work
- I would like to extend this work by keeping one central repository to store markers and IDs, instead of storing them separately on user devices.


---
**What did authors learn:**
-
**Relevant work:**
-
