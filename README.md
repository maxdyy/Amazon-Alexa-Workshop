# Alexa Skills Tech Architecture

Utterance --> Speech Streaming --> Your Service (back end) --> Response

Alexa (wake word) - open (launch) - google maps (invocation name)

# One shot example

Alexa (wake word) - ask (launch) - uber (invocation name) - for a ride (utterance)

# Utterance example

Recommend a restaurant within four miles --> { distance: 4 };
"Four" is a slot the is extracted and processed by the back end.

Tell me about Italian food within four miles --> { cosine: 'italian' }, { distance: 4 }

# Intents

AMAZON.CancelIntent \
AMAZON.HELPIntent \
AMAZON.STOPIntent

Required for certification

# Slots

{ pet } -> dog, cat, fish \
{ size } -> size, small, medium \
{ color } -> white, black, grey

I want a { pet }, that's { size } and { color }.

# Multi - Turn - Dialog

In case the user will not say everything in one sentence.

I want to order a pizza. Pizza without tomato. Big size.

A good idea is to ask for confirmations in a Multi Turn Dialog.

## Dialog Example

User: I want to order a pizza.\
Alexa: How do you want your pizza?\
User: Pizza without tomato.\
Alexa: A pizza without tomato, is that right?\
User: Yes.\
Alexa: What size?\
User: Big.\
Alexa: A big size pizza without tomato, should I place th order?\
User: Yes.

# Design Thinking

- Voice First
- Cognitive Load
- Conversational Content
- Speech

Choose voice when it is...\
**Easier** - **Faster** - **More Natural**

Choose { INVOCATION_NAME } very carefully, it cannot be changed once published.\
The { INVOCATION_NAME } should also be at least two words, unless it's a specific trademark.

Handle **Correction** from the User and **Under/Over Answering** cases.

Present Definitive Choices

Alexa: We have pepperoni and cheese. Which one would you like?/
User: Pepperoni.

Make your answers different, increase variety.

Keep the dialog simple and clear, no many choices, brief and understandable answers and interactions.\
Do not assume the user knows everything, guide the user through simple choices (even binary).

## SSML - Alexa markup language for the speech part

# Beta Functionality

Up to 500 users can Beta Test your Alexa skill.
