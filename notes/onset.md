# Onset Detection

Onset is defined as the beginning position of a note attack, which is an important feature to identify beats or segment music. To detect onsets, we usually look at a "reduced" version of original signal -- the onset envolope, and perform peak picking to localize candidate onsets. Usually the onset detection algorithms consists of three major steps: preprocessing, reduction and onset localization. In the reduction step, we need to define detection/ novelty funtions which manifests the occurence of transients. After reduction, we apply peak picking for localization.

Some recourses:
* [slides (detection function)](http://www.nyu.edu/classes/bello/MIR_files/3-novelty.pdf)
* [2005 Survey Paper](http://www.nyu.edu/classes/bello/MIR_files/2005_BelloEtAl_IEEE_TSALP.pdf)
* [2010 LSTM Paper](http://ismir2010.ismir.net/proceedings/ismir2010-101.pdf)

Categories:
* Time domain approach (rarely used, due to unreliability)
* Spectral domain approach: HFC, SF (modulus), NWPD (phase), and RCD (complex domain). HFC, SF and RCD were only looking at amplitude increase but ignoring the decrease.
* Probabilistic models
* Data-drive approach: using CNN or LSTM.