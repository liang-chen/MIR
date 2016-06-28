# Beat Tracking

For beat tracking, we need to determine both the tempo and beat locations. Tempo refers to the speed of music and is always measured as beats per minutes (BPM).

[[CAUSAL'04](http://ismir2004.ismir.net/proceedings/p033-page-164-paper226.pdf)] estimates the tempo and beats in two separate steps. The tempo is estimated from the ACF (autocorrelation function) of onset envolope convoluted with a comb filter. Beat is localized by matching synthesized comb filter from estimated tempo and onset function using cross correlation.
