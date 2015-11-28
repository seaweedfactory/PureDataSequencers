# PureDataSequencers
Alternative experimental sequencers for Pure Data (pd).

# About Pure Data Computer Music System
These sequencers are meant to be used by the Pure Data Computer Music System. This is a free and open version of the MSP environment. Pure Data is available at http://puredata.info/.

# RandomizedDivision
This sequencer chops an audio file to pieces and plays them back in a randomized order using a form of granular synthesis. The size of the pieces is a variable power of 2 division if "vary note length" is checked. It is best to start the program with this option checked. To begin using the sequencer, click the "click here to start" button. A prompt will appear for an audio file. The program is configured to use 44100 as its sample rate, this can be adjusted by changing the "/ 44.1" step towards the middle.

Check the "start playback" box to begin dividing the file. Turn the "speed" control up from 0 if no sound is heard. This is a global control over playback pitch. If "vary note length" is checked, a new divisor will be chosen at random after each grain finishes playing. If "jump to slice start" is checked, playback of the next grain will begin immediately at the grain's position. If it is unchecked, the playback counter will slide towards the grain's start position, playing samples along the way.

The array shows the contents of the sample file along with an indicator of current position.


# WeightedMatrix
This sequencer uses a probability matrix to determine when to play any of the 8 channels for each of the 16 steps. Each step has an entry for the probability of playing each channel. Enter zero to never play the step or 100 to always play the step. Entering any number in between will result in the sample sometimes playing. It will play less if the number is closer to zero.

To begin, click the yellow button on each sample channel to load an audio file. Move the "Sample Volume" slider under each channel up. This can later be used to adjust the mix. Also turn up the "Main Volume" slider. Enter a value in milliseconds to wait between steps in the "Step Delay" box.

Fill out the Probability Matrix. Click "Start Playback" to activate the sequencer.

This control uses other subcontrols: WeightedRow and WeightedSwitch.


# DelayStep8
This sequencer has a variable delay between each step. By setting different delays, swing and shuffle effects can be achieved. It is fully packaged in an 8 step, 4 channel control. 

This control set up for use in DelayStep8Example. Load samples using the yellow buttons on each channel of the "Sample Bank". Set the "Step Delay" to the desired initial delay between each step. The sliders on the control will act as an offset to this global setting. Remember to turn the "Main Volume" up. Channels are turned on for each step using the "Channel Enable" check boxes.

Click "Start Playback" to activate the sequencer.


# SimpleSampler
This control acts as a basic sample player. Click the yellow button to load samples. Click the green button to play the sample back. A pulse into the inlet will play the sample back.
