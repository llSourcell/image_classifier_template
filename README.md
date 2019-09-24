## Credits

Credits go to the FastAI team, Naveen Chanakya, and the Flutter team. I integrated a few different tutorials together to form a SaaS pipeline template. This is the code for [this](https://youtu.be/CzPYgRaYWUA) video on Youtube by Siraj Raval on building an image classification startup. There are 3 components here; A web API, a model training script, and a mobile app. The code in this repository is for the starter flutter app. Let's go through the 5 step process below. Pull Requests are always welcome!

### Step 1: Find an Image Dataset

##### What is the image classification service you'd like to build? Once you decide, find a related dataset using these tools
- [Dataset Search](https://toolbox.google.com/datasetsearch)
- [Awesome Datasets](https://github.com/awesomedata/awesome-public-datasets)

### Step 2: Transfer Learning

- Run [this](https://github.com/naveenchanakya/bear-classifier/blob/master/bear_classifier.ipynb) notebook on your local machine or upload and run it to [colab](colab.research.google.com). Replace the bear dataset with your own image dataset. It's retraining a 'resnet34' image classification model. This is transfer learning.
- Save the resulting model pkl file to google drive, save the download link.

### Step 3: Signup for Firebase + Stripe
- [Firebase](http://firebase.com)
- [Stripe](https://stripe.com)

### Step 4: Deploy the Web API 

- Fork [this](https://github.com/render-examples/fastai-v3) repository.
- Follow the instructions in its README to deploy it to render
- Once deployed, check that it works. 
- Then replace line 12 in 'server.py' of the web example with a link to your own classifier pkl file and re-deploy
- Make any cosmetic changes to the front-end inteface that you'd like

### Step 5: Build the Mobile App

- Install Flutter [here](https://flutter.dev/docs/get-started/install) 
- Download this code
- Open it in android studio as a new flutter project
- it will ask you to 'get' all dependencies, say yes and it'll will all be installed automatically
- Replace the default render link in 'main.dart' to the link to your deployed render app
- Notice the 2 functions for signup and login. This is where your stripe and firebase authentication
code will be placed
- See [this](https://firebase.google.com/docs/flutter/setup) and [this](https://pub.dev/packages/stripe_payment)

