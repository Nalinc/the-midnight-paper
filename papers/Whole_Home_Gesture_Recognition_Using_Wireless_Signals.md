## Whole-home gesture recognition using wireless signals

#### Authors: Qifan Pu, Sidhant Gupta, Shyamnath Gollakota, and Shwetak Patel

#### Conference: Mobicomp 2013, Miami, FL USA

#### Keywords: Gesture Recognition, Wireless Sensing

#### What	is	the	high-level	research question
This paper discusses the use of wireless systems to enable gesture recognition.

Such a system would enable whole-home gesture recognition using few wireless sources without the use of sensors on the human body. Also avoids the use of cameras. Thus the system is scalable and minimizes costs. 

#### Specific Research Question and Hypothesis
This paper addresses the following questions:
- How to capture information about gestures from wireless signals.
- How can we deal with other humans in the environment.

#### Key Findings
- WiSee can classify nine whole-body gestures  with an average accuracy of 94% using a 4-antenna receiver and 2 single-antenna transmitters. The accuracy decreases to 60% when one single-antenna transmitter is used.
- The average false positive rate is 2.63 events per hour when using a preamble with two gesture repetitions. This decreases to 0.07 events per hour when the number of repetitions increases  to four.
- Using a 5-antenna receiver and a single-antenna transmitter, WiSee can successfully perform gesture classification in the presence of three other users performing random gestures. The classification accuracy reduces as the number of interfering users increases.


#### Data Collection Methodologies
Received Wi-Fi signals are transformed to a narrow-band pulse (BW of a few Hz). The receiver tracks this frequency to detect small Doppler shifts associated with gestures movements. The receiver also tracks the frequency corresponding to the maximum energy and corrects for the residual frequency offset. The receiver then looks for segments corresponding to the Doppler shifts and clusters these segments into gestures. Gestures are classified by matching the pattern of positive and negative Doppler shifts.

#### Data Analysis Methodologies
To evaluate how well WiSee can detect the presence of a gesture, the Doppler SNR (the ratio between the average energy in the non-DC frequencies in the profile, with and without the gesture) is computed from the frequency-time Doppler profile. The average Doppler SNR was computed at each location by having each user repeat the gesture ten times. The experiments were carried out in the following scenarios:
- (a) A receiver and a transmitter are placed next to each other in a room. The user performs gestures in line-of-sight to the receiver.
- (b) A receiver and a transmitter are placed in adjacent rooms separated by a wall. The user performs the gestures in the room with the transmitter.
- (c) A receiver and a transmitter are placed 19.7 feet away from each other. The user performs gestures in line-of-sight to the receiver.
- (d) A receiver and a transmitter are placed next to each other close to a wall. The user performs gestures in the room adjacent to the wall.
- (e) A receiver and a transmitter are placed in different rooms separated by a corridor. The user performs the gestures in the corridor.
- (f ) A receiver and a transmitter are placed in different rooms separated by a room. The user performs the gestures in the middle room.
- (g) A receivers and 2 single-antenna transmitters placed in the living room of a two-bedroom apartment.


#### Did	the	paper	draw	convincing	conclusions	using	the	methodology?
The paper proposes a novel and efficient method to enable gesture recognition without the use of expensive and sophisticated technology. However, we do believe that the paper suffers from the following limitations:
- They only used the 5 GHz band, which does not have much interference in normal environment as not many people use it currently. It is not clear how their result would change if they used the 2.5 GHz band.
- The main point of the paper is to have a system that is widespread and easily accessible, however, since not many widespread routers support the 5 GHz band yet, it is not clear how applicable their current system is.


#### Describe	a	few	ways	in	which	the	data	collection	and	analysis	methodology	can	be improved to	better answer	the	research questions.
The authors should try to address the gesture-recognition problem using the more widely-used 2.4GHz band so as to make the technology more accessible to everyday users.

