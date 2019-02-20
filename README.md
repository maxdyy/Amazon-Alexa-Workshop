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

AMAZON.CancelIntent
AMAZON.HELPIntent
AMAZON.STOPIntent

Required for certification

# Slots

{ pet } -> dog, cat, fish
{ size } -> size, small, medium
{ color } -> white, black, grey

I want a { pet }, that's { size } and { color }.

# Multi - Turn - Dialog

In case the user will not say everything in one sentence.

I want to order a pizza. Pizza without tomato. Big size.

A good idea is to ask for confirmations in a Multi Turn Dialog.
