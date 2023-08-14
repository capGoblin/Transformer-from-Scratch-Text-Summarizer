# Transformer from Scratch for Text Summarization
Transformer built from scratch w/ Tensorflow w/o Hugging Face for Text Summarization (trained with news text)
This Jupyter Notebook demonstrates the creation of a Transformer model from scratch using TensorFlow, without utilizing the Hugging Face library.<br> The purpose of the model is text summarization, where short news articles are condensed into a single-line summary.<br>The model is trained using news text data from Kaggle's news shorts dataset.

## Preprocessing
The notebook performs the following preprocessing steps:

Tokenization: The news texts are tokenized into integer tokens for model input.<br>
Padding/Truncating: Sequences are adjusted to ensure uniform sequence lengths.<br>

## Building the Model:
The Transformer model is constructed following these key components:<br>

Scaled Dot Product: A crucial element of self-attention mechanisms.<br>
Multi-Headed Attention: Enhances model capacity to attend to different parts of the input.<br>
Feed Forward Network: A core building block of both the Transformer encoder and decoder.<br>
Encoder Layer: The fundamental unit of the Transformer encoder.<br>
Decoder Layer: The fundamental unit of the Transformer decoder.<br>
Encoder: Comprises multiple Encoder Layers.<br>
Decoder: Comprises multiple Decoder Layers.<br>
Transformer: Bringing together the Encoder and Decoder components.<br>

## Hyperparameters:<br>
The model is trained with the following hyperparameters:<br>

Number of Layers: 4
Model Dimension (d_model): 128
Hidden Units: 512
Number of Heads: 8
Epochs: 5
## Training and Evaluation:<br>
During the training process, the notebook saves checkpoint files at the end of each epoch. To evaluate the model, a summarization example is provided:

Original News:
"A historic achievement has been made in the realm of space exploration. Astronomers have detected the presence of an Earth-like planet orbiting a distant star within the habitable zone. This exciting discovery raises the possibility of finding extraterrestrial life and provides valuable insights into the existence of other habitable worlds beyond our own. Scientists are now planning detailed observations and future missions to explore this intriguing exoplanet further. The discovery marks a significant milestone in our quest to unravel the mysteries of the universe and understand our place in the cosmos."

Generated Summary:
"newly made new space detected for earth like planet"

transformer.summary()<br>
```plaintext
Model: "transformer_15"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 encoder_15 (Encoder)        multiple                  10567424  
                                                                 
 decoder_15 (Decoder)        multiple                  4854912   
                                                                 
 dense_4911 (Dense)          multiple                  3826269   
                                                                 
=================================================================
Total params: 19,248,605
Trainable params: 19,248,605
Non-trainable params: 0
