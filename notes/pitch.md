# Pitch Tracking

Here is a [link](http://miracle.otago.ac.nz/tartini/papers/Philip_McLeod_PhD.pdf) to Philip McLeod's thesis: Fast, Accurate Pitch Detection Tools for Music Analysis

Here is [code](https://gist.github.com/endolith/255291) for some of the simpler pitch-detection algorithms described below, such as zero-crossing, FFT peak, or autocorrelation.

##Zero-Crossing
Count zero-crossings in a given number of samples and compute frequency from this. 
Pro: used for basic guitar tuners
Con: inaccurate when overtones or noise cause multiple zero-crossings per period

##Autocorrelation

Autocorrelation is cross-correlation of a signal with itself. 

C(Theta) = integral -inf to +inf s(t)*s(t - Theta)

Its use is in detecting periodicities. The autocorrelation function has its maximum at 0-lag, where the value is the energy of the signal. It is symmetric around 0, because a negative lag is simply a shifted version of the positive lag.

The code below computes autocorrelation on an FFT frame to find the bin of the fundamental frequency. It keeps only the positive lags, thus discarding the first half of the correlation values. It does not use a Hamming window, but this would often be desirable.

###Pros
* Resistant to noise
* Good for lower pitches and small frequency ranges: used often for speech analysis

###Cons
* Risk of octave inaccuracy, since there can be higher peaks than the fundamental
* Requires multiple periods to be accurate (FFT frame length), so some averaging is unavoidable
* Works mainly for harmonic signals
* Resolution is dependent on sampling rate

Read about type II autocorrelation in the thesis. Here, only type I was described.
