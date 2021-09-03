# Audio-signal-classification

*Classification of audio signals from Violin, Piano and Human Voice using Machine Learning techniques.*

This is an audio signal classification project using Machine Learning techniques. The audio signals used are from Piano, Violin and Human Voice.

## Dataset

The dataset used here is part of the famous `IRMAS` dataset, that is compiled by Ferdinand Fuhrmann in his [PhD Thesis](https://ismir2012.ismir.net/event/papers/559_ISMIR_2012.pdf). We have used a sample of 1700 audio files which include Piano (600 items), Violin (580 items) and Human Voice (590 items). The orginal dataset can be obtained from the [IRMAS Dataset](https://www.upf.edu/web/mtg/irmas) .

## Feature Extraction and Classification

The code for extracting these features are given in the `Feature Extraction.ipynb` file. The python package **Librosa** was used for audio signal analysis and feature extraction. We have extracted the following 30 features from the audi signals :

* rms
* spectral_centroid
* spectral_bandwidth
* spectral rolloff
* zero_crossing_rate
* Mel Frequency Cepstral Coefficients (13)
* Chroma Features (12)

The dataset obtained after performing feature extraction is provided as `Extracted_Features.csv`.
`Machine_Learning.ipynb` contains the code for dimensionality reduction using Principal Component Analysis (PCA) and model preperaion. The final model was trained on the reduced dataset containing 20 principal components. The Machine Learning models used along with their accuracy are :

* Support Vector Machines (80%)
* Random Forest Classifier (81%)
* XGBoost (79%)
* K Nearest Neighbours (73%)


  


