## Cyclops: Wearable and Single-Piece Full-Body Gesture Input Devices

#### Authors: Liwei Chan, Chi-Hao Hsieh, Yi-Ling Chen, Shuo Yang, Da-Yuan Huang, Rong-Hao Liang, Bing-Yu Chen
#### Conference: CHI 2015, Crossings, Seoul, Korea 
#### Full-body gesture input; posture recognition; single-point wearable devices; ego-centric view

#### Strength
Cyclop's different placement options allow users to use the device according to the task at hand. This gives users the flexibility of using it to target certain gestures without compromising with the posture. For example, placing it on the chest favor head interactions and placing it around belly enable foot interactions.

- Cyclop's, different placement options allow users to use the device according to the task at hand.
- A single piece wearable device is easier to handle compared to distributed motion sensors around the body packed in (motion-capture) suits.
- Wider "field-of-view" not only captures full body gestures,but also provides dedicated interaction space.
- I like the way they simplified foreground extraction using active infrared illumination using infrared LEDs.

#### Weakness
Excluding female participants to avoid unfavourable factors in evaluation is a major drawback. If some users felt uncomfortable with putting the device on the chest, authors could have suggested placing it on belly and modify the task in pilot study to get more representative results. The claim to support different placement options is inconsistent with their discussions in different sections.

#### Possible Extension
I would extend Cyclops as an intelligent personal assistant that can not only see and classify user gestures, but also suggest actions based on users' own blind spots or things what human eyes cannot identify but infrared imaging can(for example: icy slippery surfaces).

---

Depending on purpose and application, low-level sensing techniques be implemented on certain parts of the body. However, full-body motion input requires a body sensor network of sensors that are distributed on body parts, which may be inconvenient for users to put on. Cyclops overcome this by proposing a single-piece wearable device with wider "field of view". Cyclops recognizes static and moving bodily gestures based on motion history images (MHI) and a random decision forest (RDF). 

**Hardware specifications:**
- Uses an infrared camera for foreground extraction.
- The Raspberry Pi NOIR with Super Fisheye Lens having a 235-Degree field of view.
- Five infrared LEDs attached around the lens to provide uniform illumination.
- Raspberry Pi streams images from the camera wirelessly over WiFi using the GStreamer Multimedia Framework.

**Image pre-processing pipeline:**
Basic idea is to extract foreground images from where the limbs enter the ego-centric view at the edge of the fisheye image. This strategy avoids dealing with non-limb foregrounds in the central part of the image
- First, the source images (Figure 6a) are re-oriented using the information that is pro- vided by the IMU
- The process begins from a circular strip at the edge of the fisheye image. This circular strip is then straightened.
- Then, Otsu thresholding is applied to the strip image to extract the foreground regions that potentially contain limbs.
- To separately identify limbs that overlap in the image, a vertical erosion along the length of the strip is performed to remove weak connections.
- From the geometric center of each connected component in the strip image, its corresponding position in the source image is identified, and used as a seed from which a foreground region is grown by performing image flooding.
- The Canny edge map of the source image, is utilized to block the flooding operation
- The finalized foreground masks are used to compute the MHIs.


**Relevant work:**
- Analyzing the sound that bounces through bones [14][26] al- lows tapping on the skin to be detected by acoustic sensors that are worn on the arm
- SenSkin [27] made the skin into a touch interface by sensing skin deformation that is caused by the application of a force tangentially to the skin.
- PUB [20] facilitated touch interactions on the forearm by using a dis- tance sensor on the wrist.
- Touche [30] enabled discrete hand gestures using swept frequency capacitive sensing.
- Saponas et al. [29] enabled hand gestural interaction by analyzing forearm electromyography
- uTrack [6] enabled touch interaction on the palm by magnetic localization.
- FingerPad [5] used magnetic tracking to turn the index fingertip into a touch interface
