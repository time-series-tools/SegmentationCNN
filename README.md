## Segmentation CNN

### Description
Convolutional neural networks for music segmentation following [1], with the difference that input spectrograms are max pooled across beat times. Beat tracking was done using the MADMOM toolbox (https://github.com/CPJKU/madmom) with the DBN beat tracking algorithm from [2].

On the 'Internet Archive' portion of the SALAMI dataset (https://ddmal.music.mcgill.ca/research/salami/annotations) it achieves a boundary detection f-Measure of 59% at a tolerance of +-2 beats for a random 0.9/0.1 split.

Some example outputs of the CNN with corresponding ground truth annotation can be found in the 'Results' subfolder (the nicer examples :)

### TODO 
This is work in progress! So far the feature extraction and evaluation was run in MATLAB, whereas for the CNN training, the Keras Python library was used. Evaluation is done on the beat level with a tolerance window of +-2 beats using the [Beat Tracking Evaluation Toolbox](https://code.soundsoftware.ac.uk/projects/beat-evaluation/). Currently porting the feature extraction and evaluation to Python.

### References

[1] Karen Ullrich et. al.: Boundary detection in music structure analysis using convolutional neural networks. ISMIR 2014. [pdf](http://www.ofai.at/~jan.schlueter/pubs/2014_ismir.pdf)

[2] Sebastian Böck, Florian Krebs and Gerhard Widmer, A Multi-Model Approach to Beat Tracking Considering Heterogeneous Music Styles. ISMIR 2014. [pdf](http://www.terasoft.com.tw/conf/ismir2014/proceedings/T108_367_Paper.pdf)


