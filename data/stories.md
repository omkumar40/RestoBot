## bot
* whoareyou
    - utter_iamabot

## greeting then user asking for restaurant then bot will ask the location and the cusines and will show the results
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search
    - utter_ask_location
* restaurant_search{"location": "delhi"}
    - slot{"location": "delhi"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - action_search_restaurants
* affirm
    - utter_goodbye
## greeting the user,then user would enter the cuisne, bot will ask for the location and show the results accordingly
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - utter_ask_location
* restaurant_search{"location": "Delhi"}
    - slot{"location": "Delhi"}
    - action_search_restaurants
* affirm
    - utter_goodbye

## location specified with the user query before and then specifying the cuisine
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search{"location": "delhi"}
    - slot{"location": "delhi"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - action_search_restaurants
* affirm
    - utter_goodbye

## greeting, then asking the bot what it can do, asking for some restaurants in a location, bot will ask for the cuisines and show results
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search{"location": "delhi"}
    - slot{"location": "delhi"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "North Indian"}
    - slot{"cuisine": "North Indian"}
    - action_search_restaurants
* affirm
    - utter_goodbye


## user will specify both the cuisine and the location of the restaurant user wants, then accordingly the results would be printed
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search{"cuisine": "chinese", "location":"delhi"}
    - slot{"cuisine": "chinese"}
    - slot{"location":"delhi"}
    - action_search_restaurants
* affirm
    - utter_goodbye

## user asking about a bot and askig for a specific cuisine, bot will ask for location and show the results
* greet
    - utter_greet
* whoareyou
    - utter_iamabot
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - utter_ask_location
* restaurant_search{"location": "Delhi"}
    - slot{"location": "Delhi"}
    - action_search_restaurants
* affirm
    - utter_goodbye
