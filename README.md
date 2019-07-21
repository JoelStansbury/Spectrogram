# Spectrogram
Functions for converting Audio -> Spectrogram and Spectrogram -> Audio

## Functions
`spectrogram(y,sr)` - Converts a waveform `y` of sample rate `sr` into a spectrogram image. _Returns 2D-np.array()_

`spec2wav(arr)` - Generates a waveform from the given spectrogram `arr`. _Returns 1D-np.array()_

* _note_ `spec2wav` depends on the simplistic aproach of `spectrogram` and will likely not behave correctly with other spectrogram generators

<details>
When making a spectrogram, a typical approach is to use a window length of 0.25 seconds and step 0.01 seconds for each column of pixels, i.e. there is some overlap. My generator has no overlap, so `spec2wav` expects no overlap and will not perform correctly on those which do.
</details>

## Dependencies
* Scipy
* Numpy
* Matplotlib

## Description
In a nutshell, I'm experimenting with spectrograms as a way of editing waveforms. In some ways, a spectrogram resembles the kind of interface you may have when editing midi files. You can see what frequencies are present at any moment in time, so if you want to remove only some of the noise in a given moment you can simply edit the spectrogram to set those frequencies (pixel values) to zero.

One of the cool things this allows us to do is apply a gaussian filter across frequency and time. I suppose the effect is subjective, but to me this strengthens the illusion of being in the room where the sound was produced, similar to reverb but more natural.

See the iPython notebook for illustrations and examples. Unfortunately some parts of this notebook do not work on github, namely the audio playback. I'll work on moving those illustrations into this readme
