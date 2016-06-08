# Pitch Tracking

##Autocorrelation

Autocorrelation is cross-correlation of a signal with itself. 

C(Theta) = integral -inf to +inf s(t)*s(t - Theta)

Its use is in detecting periodicities. The autocorrelation function has its maximum at 0-lag, where the value is the energy of the signal. It is symmetric around 0, because a negative lag is simply a shifted version of the positive lag.

The code below computes autocorrelation on an FFT frame to find the bin of the fundamental frequency. It keeps only the positive lags, thus discarding the first half of the correlation values. 

[code (auto-correlation)](https://gist.github.com/endolith/255291)
