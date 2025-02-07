# Audio Classifier Using DL

Dataset: [gtzan-music-speech](http://opihi.cs.uvic.ca/sound)

An audio classifier that is capable of classifying an audio as music or speech. The dataset consists of 128 tracks, each 30 seconds long. Each class (music/speech) has 64 examples. The tracks are all 22050Hz Mono 16-bit audio files in .wav format. 

The raw audio is processed using discrete Fourier transform. This will return complex coordinates (real and imaginary) which will be then converted into cartesian coordinates indicating magnitude and phase. Finally the resultant values will be converted to a pseudo decibel scale. All these values will be plotted on a Frequency vs Time graph. 

A sliding window is created that will snap the Xs and ys (one-hot encoding) of the graph every 250 ms. These values will be store in a list as inputs and labels for the network. All the collected inputs and labels will then be fed to the network (4 layer CNN + 2 fully connected layer).
