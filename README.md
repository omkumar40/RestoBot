# RestoBot
A restaurant bot made with help of Python's Rasa Library, which uses the Zomato API to find the restaurants from a given location.

User is giving input to what type of food he/she would like to have with the input of their location and using the Zomato API, The results whill be showed on the screen.

## See the GIF below!

![SS1](https://github.com/omkumar40/root/blob/master/Anaconda%20Prompt%20(anaconda3)%20-%20rasa%20%20shell%202021-01-25%2017-12-30.gif)
![SS2](https://github.com/omkumar40/root/blob/master/Anaconda%20Prompt%20(anaconda3)%20-%20rasa%20%20shell%202021-01-25%2017-18-21.gif)

### If you don't have rasa installed then follow this link for easy installation [Youtube link](https://www.youtube.com/playlist?list=PL75e0qA87dlEWUA5ToqLLR026wIkk2evk)

## How to use
* Clone the repo
* add the Zomato API key to zomatopy.py file
* open the terminal in the project directory and run the below commands
## rasa train
Once the bot has been trained, run the bot using the below commands:- 
## rasa run actions
## rasa shell

## What is Rasa
Rasa is a framework for developing AI powered, industrial grade chatbots. It's incredibly powerful, and is used by developers worldwide to create chatbots and contextual assistants. 
## What is Rasa NLU
Rasa NLU is primarily used to build chatbots and voice apps, where this is called intent classification and entity extraction. To use Rasa, you have to provide some training data. That is, a set of messages which you've already labelled with their intents and entities. Rasa then uses machine learning to pick up patterns and generalise to unseen sentences.

## What is Rasa Core
Rasa Core is a dialogue management solution tries to build a probability model which decides the set of actions to perform based on the previous set of user inputs.


## Difference between NLU and Core
Rasa NLU’s job is to interpret messages, and Rasa Core’s job is to decide what should happen next.
Rasa NLU: It's the interpreter who understands the input. Basically figures out entities and labels the intent.
Rasa Core: It does the rest of the work you want your bot to do. The flow of conversation is the most important thing.

## Now let's learn the terminologies we have in our chatbot
* <b>Intent</b> - It refers to what a person is trying to say. For eg:'I want to order chinese food', here the intent is to order some food
* <b>Entity</b>-  An entity in a chatbot is used to add values to search the intent. For eg: The intent is to order some food, but the entity is chinese which is of the type cuisine
* <b>Actions</b> - Declarations of functions that will be called when the intents, entities and entity types in a sentence are identified.
* <b>Stories</b> - The flow of conversation is defined by a story. For eg: how will the chat communicate after greeting
* <b>Slots</b>- Slots are the variables you give your program to let your bot categorize and interpret users' input.
* <b>Responses</b> - Definition of some not all actions.

## Now the set of documents which we will be having
* domain.yml- defines chatbot domain like entities, actions, templates, slots
* config.yml- contains model configuration and custom policy
* credentials.yml- contains authentication token to connect with channels
* endpoints.yml- contains the webhook configuration for custom action
* nlu.md - contains training examples for the NLU model
* stories.md - ontains training stories for the Core model
* actions.py : contains the following custom actions (insert ZOMATO API key in this script file before starting RASA server):-
  1. searches a restaurant with some specific cuisine in a location
  2. Displays the top 5  restaurant details to the users
