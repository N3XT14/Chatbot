# Chatbot

Hi bots :)

In this repository you will find all the information needed to build a simple yet an awesome chatbot. So, let's dive into the making.

### Data Source:  


Toke> nizers divide strings into lists of substrings. For example, tokenizers can be used to find the words and punctuation in a string:


`* Intent.json` 
* An array of objects containing various parameters such as tags, patterns, responses, links, and contexts that will help model to predict the response based on the tag and pattern it belongs to.
* For each pattern we will create a 2d document having tokenized words, and the tag it belongs to for our training set.

### Pickle Module:
> A PKL file is a file created by pickle, a Python module that enabless objects to be serialized to files on disk and deserialized back into the program at runtime. It contains a byte stream that represents the objects.

`* words.pkl`
  * Contains tokenized words from the patterns present in the intent object.
  
`* classes.pkl`
  *  Contains set of tags from the intent object. 

### Packages and Modules:
#### NLTK

`* word_tokenize`
  * Tokenizers divide strings into lists of substrings. For example, tokenizers can be used to find the words and punctuation in a string:

`* WordNetLemmatizer`
  * Exposes method that helps in lematization. It links words with similar meanings to one supporting morphological analysis of the words.
      
#### KERAS

`* Sequential Model`
  * Model appropriate as we have single input and output tensor.

`* Parameters: Dense, Activation, Dropout`
  * Dense:
    * A regular deeply connected NNL. It implements the operation on the input shape based on the activation function having as an argument.
    
  * Activation:
    * The function which determines the transformation of the inputted node to the outpute node in that particular layer.
    * RELU:  If input > 0 then output = input else output = 0.
  
  * Dropout:
    * The Dropout layer randomly sets input units to 0 with a frequency of rate at each step during training time to prevent overfitting. 
    * This helps in averaging the nerual networks. In simple words, the dropout drop some of the nodes from the hidden layers.

 `* Optimizer: SDG`
  * An optimizer over the normal gradient descent technique to select a sample of dataset instead of whole.
  * To get the minima of the cost fucntion

Once the model is create, we can proceed in creating the GUI for the chatbot:

1. At first we will register the user message and pass it to our function predict_class.
 
    * It will return a 2D list having tags at 0 index and probability of its belonging at index 1.
    * The list will be a reverse sorted list based on the threshold value that we get after model prediction.

2. Next, the list will be passed to the function getResponse where in we will match the tag and on a match a response will be selected randomly from the response list.

3. At last, we are creating a satisfactory table of our bot based on the user response.

Thats it. Thats all you need to create a chatbot. Thanks for reading.

# Happy Coding !!!!
