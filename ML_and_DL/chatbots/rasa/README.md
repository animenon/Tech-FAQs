# RASA Open Source - a conversational AI framework for building contextual assistants

Rasa Open Source includes

- NLU: determines what the user wants and captures key contextual information
- Core: selects the next best response or action based on conversation history
- Channels and integrations: connect assistant to users and backend systems

Rasa X is a toolset that helps you leverage conversations to improve your assistant.

## Commands

Initialize a new rasa project, this setsup a basic chatbot with few default intents and utterences(responses):

    rasa init

It asks for location where project should be created, just click `Enter` to create in the current
 directory or you may specify the new location. `--no-prompt` flag can be used to avoid these.

To start a rasa interative session with trained model :

    rasa shell

To train a model:

    rasa train


## Files in a rasa project

- data
    - `nlu.md` - NLU training data
    - `stories.md` - all stories go here
- models - `tar.gz` with models are stored in here
- tests - all test files in here
- `actions.py` - code for your custom actions
- `domain.yml` - assistant’s domain(what user inputs it should expect to get, what actions it should
                 be able to predict, how to respond, and what information to store)
- `config.yml` - configuration file defines the NLU and Core components that your model will use
- `credentials.yml` - details for connecting to other services
- `endpoints.yml` - details for connecting to channels like fb messenger


