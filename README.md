# Text-To-User-Predictor-NLP

# What it is?
The goal of this project was to identify the author of some text. Specifically, this project takes text and identifies which of my discord friends would be its author.

## Data Collection
I web scraped message data from a discord group chat using a python script that I created using beautiful soup. I collected message content and who sent each message.

## Data Preprocessing
I cleaned the data and converted my friends' into numerical targets which the model could output. I took a stratified sample of the data to ensure that each of my friends was represented equally. This also prevented the model from just outputting the most common discord friend in the data as an author to achieve a high accuracy even though the output would be essentially useless.

##NLP Model Creation
I created a custom text vectorizer and embedding layer to go from strings of texts to arrays which represented the text which allowed the data to be understood by the computer. I created these instead of using pre-trained embedding layers such as the Universal Sentence Encoder because I wanted a more light weight model. I also wanted to ensure that the unique slang used in my group would be appropriately converted to matrix representations. I then created a network of LSTM and Dense layers in a TensorFlow sequential model. All of this was then combined into one model and then trained to output a probability model on how likely it is for each of my friends to say an input sentence.

## Test it out here!
[DiscordNLP Website](http://armohammed.tech/discord-project-nlp/)


## Usage
1. Create a `sample.json` file from text data from users and format it like `example.json`.
2. Replace class_names list with a list of the different names from your dataset, make sure each index is mapped correctly (so if friend1 is 0 in the data table, assign them as the first name in the list)
3. Run the code and choose the best performing model for your project
