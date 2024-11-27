## SC4002_Project

### Packages to install using pip:
datasets\
nltk\
Contractions\
fastText

### Files:
Main Copy.ipynb - to address all the parts except for Part 3.5\
Enhancement.ipynb - to address Part 3.5

### Instructions to run the code:
For the notebooks, just choose the option to ‘Run All’. Preferably, run Main Copy.ipynb first before running Enhancement.ipynb.

### Main Copy.ipynb
Table of Contents: 

*Part 0*
Installed “datasets” library.
Loaded ‘Movie review’ dataset into train, validation and test datasets.

*Part 1(a)*
Imported “nltk”, “contractions” and other relevant libraries.\
Processed and tokenized the training data before computing the size of vocabulary formed from training data.

*Part 1(b)*
Downloaded Glove pre-trained embeddings.\
Computed the number of out-of-vocabulary (OOV) words.

*Part 1(c)*
Installed “fastText” library.\
Trained supervised and unsupervised models to provide word embeddings of unknown words. \
Implemented code to handle OOV words using fastText and remove OOV words less than MIN_COUNT.

*Part 2*
Plotted the distribution of Movie Review Lengths and retrieved the maximum length of input sequences for model training.\
Pre-processed the text from train, validation and test datasets into word embeddings to be used in training, validation and testing of models.\
	Model Training:\
	Outputted the train, validation and test accuracies of the following models after determining the optimal configuration and training of the models
		- Train the RNN with last hidden state
		- Train the RNN with max pooling
		- Train the RNN with average pooling
		- Train the RNN model with the concatenation of average and max pooling

*Part 3*
Outputted the train, validation and test accuracies of the following models after determining the optimal configuration and training of the models
	- Trainable Layers
	- Training of RNN with OOV being handled
	- biLSTM
	- biGRU
	- CNN
	- Enhancement - Ensembling Method


### Enhancement.ipynb
Table of Contents:
1. Loading of Dataset, Tokenizer and Model
2. Base Model Inference
	- Prints test accuracy of the base model
3. Fine Tuning
	- LoRA Config
	- Training Config
	 	- outputs the trained adapter to lora/ folder
	- Inference
		- load and merge adapter from lora/ folder for inference
		- Prints test accuracy of fine-tuned model
