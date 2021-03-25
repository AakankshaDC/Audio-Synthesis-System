# Audio-Synthesis-System

The physical modeling of complex sound generators can only be approached by individually synthesizing and discretizing the objects that contribute to the generation of sounds. This raises the problem of how to correctly implement the interaction between these objects.

In the past decade, the market has been preparing itself for the maturing of the technology related to the creation of interactive multimedia environments.

Inspite of the abundance of results in the many areas of interest for multimedia applications, little has been done for synergically exploiting those that concern synthetic and natural modeling/rendering of acoustic 3-D environments.

This environment is based on a foundation structure consisting of a small number of Java interfaces abstract classes, and a potentially unlimited number of unit generators, which are created by extending the abstract classes and implementing a single method.

Filter-graphs, sometimes called “patches”, are created by linking together unit generators in arbitrary complex graph structures. Patches can be rendered in real-time with special unit generators that communicate with the audio hardware, which we have implemented using the JavaSound API.	

# Implementation

Java classes preferred here are: AudioFormat, AudioInputStream and SourceDataLine.

Inputs are Frequencies, Sample Rate (The higher the sampling rate, the more samples are required for a fixed amount of time, the more memory is required, and the more computational demands are placed on the computer to be able to handle the audio data in real time) and Number of channels (Mono and Stereo). Java SDK 1.4.1 allows both monaural (one channel) and stereo (two channel) sound.

Variables used in this project are:
•	sampleRate: (Every signal is represented in form of numbers i.e. the amplitude of the signal at different, uniform instances of time known as samples, the rate is known as sampleRate) Allowable 8000,11025,16000,22050,44100
•	sampleSizeInBits:  (PCM encoding is used wherein the magnitude of the analog signal is sampled at regular to obtain samples)Allowable 8,16 
•	channels: Java allows 1 or 2 
•	signed: JAVA allows only positive values of frequencies. 
In this project, there are 5 types of sound synthesized by changing the frequencies of sine wave. They are 
•	Tones
•	Stereo Panning
•	Stereo Ping Pong
•	FM Sweep
•	Decay Pulse
