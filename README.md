# QnA-ChatBot
A 'Yes' and 'No' chatbot created by performing NLP on Meta's bIbA database using End-To-End Networks based Deep Learning models.

## Overview-

Created a ChatBot that can answer questions based on a short ‘story’ i.e. a meaningful sequence of simple, descriptive sentences. 

### NLP Pipeline

1. Load and explore the Data
2. Create Vocabulary
3. Vectorization
4. Building the Model

Explaining the model in brief; we receive an input set (the stories; each collection of sentences)- x1, x2, ….,xn and we encode them into Memory vectors. We then obtain the Question q and also embed it in the form of a vector. We take Inner product of both and pass it to a softmax function.

We then obtain the Output memory representation for each input in the form of ci (c1, c2, c3….cn), upon which we perform weighted sum, and the weights are supplied by the probability distribution of inputs to obtain oi.

Finally using the input layer and oi, along with a weight matrix W, we get the Single layer case by performing -
a = Softmax(W(o+u))

This gives us the final probability of the predicted answer.

We then expand this process into Multiple layers by using Recurrent Neural Networks, wherein we take the output of a single layer and feed it as the input to the next layer.



