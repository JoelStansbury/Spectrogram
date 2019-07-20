# Spectrogram
Functions for converting Audio -> Spectrogram and Spectrogram -> Audio

## Dependencies
* Scipy
* Numpy
* Matplotlib

## Description
In a nutshell, I'm experimenting with spectrograms as a way of editing waveforms. In some ways, a spectrogram resembles the kind of interface you may have when editing midi files. You can see what frequencies are present at any moment in time, so if you want to remove only some of the noise in a given moment you can simply edit the spectrogram to set those frequencies (pixel values) to zero.

One of the cool things this allows us to do is apply a gaussian filter across frequency and time. I suppose the effect is subjective, but to me this strengthens the illusion of being in the room where the sound was produced, similar to reverb but more natural.

See the iPython notebook for illustrations and examples. Unfortunately some parts of this notebook do not work on github, namely the audio playback. I'll work on moving those illustrations into this readme
