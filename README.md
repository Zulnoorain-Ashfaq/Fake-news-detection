# NewsDetector
NewsDetector is a PyTorch module for text classification. It utilizes an Embedding layer to convert the input text into a dense vector representation, an LSTM layer to capture the sequential information in the text, and two fully connected (Linear) layers to perform the final classification.

## Inputs
* vocab_len: The number of unique words in the vocabulary
* len_doc: The maximum length of the input documents
## Outputs
* A scalar value between 0 and 1 representing the probability of the input text belonging to the positive class.
## Methods
### forward:
* the forward method takes in a tensor of shape (batch_size, len_doc) and returns a tensor of shape (batch_size, 1) representing the probability of each input text belonging to the positive class.
The module also applies dropout with a probability of 0.3 and Leaky ReLU activation function for the final classification and sigmoid for probability output.