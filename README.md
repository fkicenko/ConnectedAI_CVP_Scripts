# ConnectedAI_CVP_Scripts
Call Studio Scripts for Dialogflow and Microsoft using uniMRCP

These 2 archives contain Call Studio 11.6 scripts. The scripts are designed to create a flow-through conversation with either Dialogflow
or Microsoft. Each script starts off by playing an opening prompt (optional) and then listening to the caller. This is done through
the 'Form' element. The form element contains a new grammar as show below;

- builtin:speech/transcribe

This grammar command is new to 11.6 and therefore you will need to apply ES82 to your CVVB server.

Once the caller finishes speaking, we receive the ASR results in text and pass it via REST to either Dialogflow or Microsoft.

Each of them will return a response to the spoken utterance which we will examine. We really only examine the response so we can 
see if a 'keyword' was sent back to us. Keywords are used to finnish the call, transfer to an agent or some other action you may 
want CVP to take.

If no keyword has been found, we simply play the response back to the caller and start the loop all over again.

Disclaimer: 
The code and examples presented above are only samples and are NOT guaranteed to be bug free and production quality.
The sample applications are meant to:
•	Illustrate how to use the relevant APIs and SDKs 
•	Serve as an example of the step by step process of building applications and architectures to accommodate the above.
•	Provided as a guide for a developer to see how to use the APIs and SDKs to customize for their own use.

