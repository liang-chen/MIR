# Beat Tracking

Beat measures how a human listener would tap his foot with music. For beat tracking, we need to determine both the tempo and beat locations. Tempo refers to the speed of music and is always measured as beats per minutes (BPM).

[[CAUSAL'04](http://ismir2004.ismir.net/proceedings/p033-page-164-paper226.pdf)] estimates the tempo and beats in two separate steps. The tempo is estimated from the ACF (autocorrelation function) of onset envelope convoluted with a comb filter. Beat is localized by matching synthesized comb filter from estimated tempo and onset function using cross correlation.

[[CONTEXT_DEPENDENT'07](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.217.5988&rep=rep1&type=pdf)] and [[TWO_STATES'05](http://telecom.inesctec.pt/~mdavies/pdfs/DaviesPlumbley05-icassp.pdf)] used two-state model to adapt to different tempos and keep producing the consistent beats in constant tempo area. The model contains both a general state using flat weighting function and a context-dependent state using constrained Gaussian weighting over the tempo strength function.

[[DP'07](https://www.ee.columbia.edu/~dpwe/pubs/Ellis07-beattrack.pdf)] formulated the problem as global optimization and performed inference by dynamic programming.

[[REALTIME'09](http://eecs.qmul.ac.uk/~markp/2009/StarkDaviesPlumbley09-dafx.pdf)]: real-time beat tracking and its application.