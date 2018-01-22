## Priming Drivers before Handover in Semi-Autonomous Cars

#### Authors: Remo M.A. van der Heiden, Shamsi T. Iqbal, Christian P. Janssen
#### CHI 2017, Denver, CO, USA
#### Keywords: Human information processing; [User Interfaces]: Benchmarking; [Robotics]: Autonomous vehicles

#### What	is	the	high-level	research question.
What are the effects of early warnings, or pre-alerts, on handover performance?
Pre-alerts are important in situations where an autonomous vehicle is unable to operate safely and requires intervention from the human driver.

#### Specific Research Question and Hypothesis
- RQ1: What do drivers do before handover?
  - how do pre-alerts affect behavior before take-over including eye-gaze and suspension of the non-driving task?
- RQ2: How do drivers experience the handover?
  -how do drivers perceive the pre-alerts?
- RQ3: How successful is the handover?
  - how do the pre-alerts affect driving performance?

#### Key Findings
- RQ1: In the single-task scenario, there is not much variation in the amount of time spent looking at the road for the various alert conditions. In the dual-task scenario, drivers look more frequently at the road in the pre-alert phase as compared to the absence of any pre-alert. Drivers disengaged from the secondary task faster in the pre-alert condition (twice as fast in the case of increasing pulse pre-alerts) as compared to the no pre-alert condition with disengagement being slightly faster for the calendar task.
- RQ2: Some drivers preferred the increased sense of urgency conveyed by the increasing pulse pre-alert while others found it annoying and preferred the repeated burst pre-alert. Also, heart rates are slightly increased in dual-task conditions.
- RQ3: Most drivers respond timely in both no pre-alert and pre-alert conditions, with pre-alert conditions involving a more timely response. In single-task situations drivers are able to respond more effectively regardless of the presence of pre-alerts. On the other hand, for dual-task situations, there is a delay in the brake response when there is no pre-alert. There is also no correlation between unsafe behavior and number of tasks. 

#### Data Collection Methodologies
Study was conducted on twenty four drivers who were selected by quota-sampling. Participants performed two types of tasks: driving(part manal and part autonomous) and a non-driving task on mobile phone. 
- Eye tracking was collected: “Looking at the road” defined as at least one eye being tracked, “not looking at the road” moments when no eyes were tracked.
- Heart rate was collected: 1 value logged/sec. 
- User preferences using a 5 point scale questionnaire. 
- Disengaging from secondary task using logs of touchscreen keypresses.
- Initial reaction time: interval between automation being disabled and first action from driver
- Driver speed reduction
- Unsafe incident analysis: manually labelled whether observed behavior was unsafe

#### Data Analysis Methodologies
Authors used a 3 (pre-alert) x 2 (number of tasks) within-subjects analysis of variance (ANOVA) with an alpha-level of .05 for significance. They used Holm-Bonferroni-corrected post-hoc tests.

#### Did	the	paper	draw	convincing	conclusions	using	the	methodology?
Results of this paper are only convincing within the limited set of methodologies and under specific conditions under which they performed the experiment. There exists fundamental problems that are not addressed, which could improve how convincing the paper is to readers:
- The paper lacks clear justification for the authors choice of 20 seconds as an interval to begin the pre-alert. The authors neglected testing this in comparison with other time intervals.
- Justification is also lacking for the types of alert chosen; i.e. “repeated burst audio pre-alert”, “increasing pulse audio pre-alert”.
- Do not address the limitation of being unable to predict “urgent” situations 20 seconds in advance (a significant amount of time at high driving speeds). e.g. how can they detect a dog running out in front of a car 20 seconds before the dog acts? There are few use cases where this technique may actually be plausible.
- Only very simplistic driving scenarios were considered (i.e. country road with bends or straight road with no intersections). Since the task was simulated and the scenarios were simplistic, participants were more likely to engage in risky behaviour, therefore it is unclear whether or not these results can be generalized to real-world situations.

#### Describe	a	few	ways	in	which	the	data	collection	and	analysis	methodology	can	be improved to	better answer	the	research questions
- Due to between-subjects nature of the study, results might be influenced due to learning effects. An ideal evaluation would have involved different participants subjected to different conditions. 
- Eye tracking results only gave insights to whether or not drivers were looking at the road, but did not infer where they were actually looking(phone screen/talking to a co-passenger). Researchers might have gathered useful results by trying different types of pre-alerts(audio signals, visual cues on display, voice-based commands) depending on what type of secondary task the driver is involved in(talking to a person, watching a video or setting calendar).


