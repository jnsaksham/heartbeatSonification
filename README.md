# heartbeatSonification
A body-music performance system that sonifies heartbeat via a santoor playing robot.

## Overview
The system is designed to sonify biofeedback for heartrate training. It reads a user's heartbeat and sonifies each beat via a santur (Iranian string instrument) playing robot with a delay. The working maxpatch can be found in the master branch

## Requirements
1. OpenBCI sensing devices. System has been tested on Ganglion and Cyton but any device compatible with OpenBCI GUI should work.
2. MaxMSP: Music generation

## Steps
1. Read ECG using OpenBCI GUI. 
2. Setup communication protocol (OSC/ UDP) between OpenBCI GUI and Max over some IP.
3. Heartbeat extractor in Max (based on dynamic thresholding of ECG signals)
4. Note selection: Markov model trained in MaxMSP on a self annotated dataset.
5. Rhythmic improvisation: Stochastic improvisation for changing note density (tremolo, double beat, etc) or delay time between the call and response.

Video
System description with melodic + rhythmic improvisation: https://www.youtube.com/watch?v=PJVbVOFOZKk
^ Skip to 1:52 for sample generation.
