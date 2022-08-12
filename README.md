# Omega
A chat-bot using PyTorch and Deep Learning &amp; integrated to a website using Flask &amp; JavaScript.

*Note: Following commands are best suited for Linux. However there might not be any drastic changes in commands for other OS like Windows.

// Create virtual environment for better setup
$ python3 -m venv venv
$ source venv/bin/activate

// Install dependencies (easy)
$ pip install -r requirements.txt

----------------------------------------------------------------------
// Install dependencies (manually if above fails)
$ (venv) pip install Flask torch torchvision nltk flask-cors
----------------------------------------------------------------------

// Install nltk packages from the terminal itself
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')

// Run	--> will dump data.pth file.
$ (venv) python train.py

// To test in console!
$ (venv) python chat.py

// File structure:

model.py        --> Pytorch model, simple NN with few linear layers
data.pth        --> Trained model
chat.py         --> Mostly used after training
intents.json    --> Modification of chatbot responses here!
                    - Re-train your model after modification: $ python train.py
	tags:       --> (Overall tag)
	patterns:   --> (To be used by user)
	responses:  --> (To be used by chatbot randomly)
