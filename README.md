# Sz-Managing-Generics-and-Resetting-Generics
Where to see the generics, change the values and reset those that have gone generic

## Viewing Generic Thresholds
Open a command prompt to the Senzing Project directory \
Source the setupEnv file

    source setupEnv

Change to the python directory

    cd python
    
Start the G2ConfigTool.py

    python3 G2ConfigTool.py

Run the command "listGenericThresholds"

    listGenericThresholds

Example Return

    (g2cfg) listGenericThresholds \

    {'plan': 'load', 'behavior': 'NAME', 'candidateCap': 10, 'scoringCap': -1, 'sendToRedo': 'No'}
    {'plan': 'load', 'behavior': 'F1', 'candidateCap': 5, 'scoringCap': 5, 'sendToRedo': 'Yes'}
    {'plan': 'load', 'behavior': 'F1E', 'candidateCap': 5, 'scoringCap': 50, 'sendToRedo': 'Yes'}
    {'plan': 'load', 'behavior': 'F1ES', 'candidateCap': 5, 'scoringCap': 50, 'sendToRedo': 'Yes'}
    {'plan': 'load', 'behavior': 'FF', 'candidateCap': 10, 'scoringCap': 30, 'sendToRedo': 'Yes'}
    {'plan': 'load', 'behavior': 'FFE', 'candidateCap': 10, 'scoringCap': 500, 'sendToRedo': 'Yes'}
    {'plan': 'load', 'behavior': 'FFES', 'candidateCap': 10, 'scoringCap': 500, 'sendToRedo': 'Yes'}

## Changing Generic Thresholds

**NOTE: CHANGES FOR GENERICS SHOULD NOT BE DONE UNTIL YOU HAVE DISCUSSED THIS WITH SENZING SUPPORT AND YOU UNDERSTAND THE IMPACTS**

Open a command prompt to the Senzing Project directory \
Source the setupEnv file

    source setupEnv

Change to the python directory

    cd python
    
Start the G2ConfigTool.py

    python3 G2ConfigTool.py

Run the command "listGenericThresholds"

    listGenericThresholds

Identify the string you wish to change \
As an example lets change F1 "Load" candidateCap from 5 to 10

    {'plan': 'load', 'behavior': 'F1', 'candidateCap': 5, 'scoringCap': 5, 'sendToRedo': 'Yes'}

You will need to edit the string by \
- adding the command "setGenericThreshold" to the beginning
- replacing the single quotes with double quotes
- and the value of the candidateCap to 10 \

Then paste the command into the prompt for the G2ConfigTool.py

    setGenericThreshold {"plan": "load", "behavior": "F1",   "candidateCap": 10,  "scoringCap": -1, "sendToRedo": "Yes"}


Save and close the G2ConfigTool.py

