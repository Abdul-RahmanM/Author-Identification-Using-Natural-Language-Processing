# Text-To-User-Predictor-NLP

## What it is?
This project uses NLP models to identify the person who most likely said a sentence. The functioning prototype uses data from my discord friends.

## How was it made?
For the demo below, I webscraped data from a discord group chat with friends and trained an NLP model to try to identify who said what!

## Test it out here!
[DiscordNLP Website](http://armohammed.tech/discord-project-nlp/)


## Usage
1. Create a `sample.json` file from text data from users and format it like `example.json`.
2. Replace class_names list with a list of the different names from your dataset, make sure each index is mapped correctly (so if friend1 is 0 in the data table, assign them as the first name in the list)
3. Run the code and choose the best performing model for your project
