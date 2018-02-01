## FrameWire: a tool for automatically extracting interaction logic from paper prototyping tests

#### Authors: Yang Li, Xiang Cao, Katherine Everitt, Morgan Dixon, James A. Landay
#### CHI 2010, Atlanta, Georgia, USA.
#### Keywords: Paper prototyping, programming by demonstration.

#### Strength
I like the way FrameWire proposes suggestive transitions for common tasks that might not be covered by limited user-defined functional transitions during the paper prototype tests. This brings an intelligence to system and imply that FrameWire is not only a wire-framing tool, but an intelligent system that senses interaction flow of designers.
- Allows designers to analyze and communicate a design and test findings to a wider audience while still allowing fluid and rapid iteration on a design using paper prototyping.
- Allow a designer to easily analyze and communicate test video by viewing generated statistics and by directly
indexing video segments related to each interaction behavior.
- Transform a paper prototype into an interactive HTML- based prototype in a semi-automatic way.
- FrameWire proposes suggestive transitions for common tasks that might not be covered by limited user-defined functional transitions during the paper prototype tests.

#### Weakness
Framewire only seem to capture "discrete interactions" like one-time clicks to transition from one state to another. These clickable areas are translated to "hot areas" of hyperlinks in generated HTML. However, in practice, users might perform other kinds of "continuous interactions" like dragging an item or scrolling the view. Framewire does not capture these interactions.

- Does not cover every interaction that are possible with an interface like hover and scroll.
- 

#### Future Work
- I would be interested in extending Framewire to capture "continuous interactions" like dragging an item and scrolling the view that happen over a sequence of time, and translate these gestures to respective actions in generated HTML.

---
**System Description**
- A system that provides a high level, structural view over one or more paper prototype test video clips and generates interactive HTML-based prototypes from these clips.
- Automatically extracts the interaction logic from raw video clips of multiple paper prototyping tests.
  - Requires a user to wear an inexpensive, commercially available, blue rubber finger tip to indicate the cursor and to dwell for a short period of time for a click action.
  - Designers can import the video clip into FrameWire for analysis.
  - Automatically extracts interface screens, user clicks and the transitions between screens from the clips.
- In the main canvas, FrameWire shows the extracted logic as an interaction flow graph.
  - In Segment View, FrameWire only shows video segments that contribute to extracted screens and transitions.
  - In the Timeline View, FrameWire shows the entire clip, including the frames in which a designer adds, removes and positions paper mockups, which do not contribute to the extraction.
- If the automatic extraction does not fully capture the designer’s intent, the designer can interactively refine and annotate the extracted logic via 'Extraction slider'. 
  - The value of the Extract slider globally determines how similar two frames must be to be considered repetitions of the same screen.
 - Generated HTML prototype uses each screen as the background image of an HTML page and overlays clickable "hot areas" of hyperlinks for the transitions, which correspond to the blue patches generated in FrameWire.


**Relevant work:**
-
