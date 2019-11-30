# audGrav
-

audGrav is a compositional tool, implemented in python, that allows a user to algorithmically edit and rearrange audio clips, both in time and space, using the equation of gravity. 

After the audio file is read, the program, with user-defined attack and release thresholds, will edit out each audio event and treat it as an independent body. An audio event, in this case, is defined as a section of audio that is preceded and followed by the noise floor of the original sound file. The equation of gravity is used to create a relationship between each audio event based on its mass and distance from other events. For our purposes, mass is equated as the RMS value of each individual audio event, and the distance is the time, in seconds squared, in between each events peak index. When actually calculating gravity, we would multiply the equation by the gravitational constant ($9.81 m/s^2$). Since audio has no gravitational constant this parameter is exposed to the user to affect how dramatic the shifting is. The end result is a new audio file with events that have shifted in time and space (stereo panning) based on mass and distances. 
