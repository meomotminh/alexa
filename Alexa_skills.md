- Define the request the skill can handle
- Define the name Alexa uses to identify your skill
- write the code to fulfill the request


pre-built model:
- alexa skill kit (ASK) defines set of words users say to invoke a skill

## Smart Home Skills
control smart home devices, gives u less controll over a user's experience but simplifies dev because u don't need to create the VUI yourself

## Flash briefing skills
provide ur users with news headlines and other short content,. define content feeds for the requested flash briefing

## video skills
provide video content. as skill dev, u define the request the skill can handle, and how video content search results display on Alexa-enabled devices

## music skills
provide audio content,

Launch the skill _ alexa, open Hello World -> sends Alexa service in the cloud -> Alexa send JSON request to handle the intent to the resource compute service that hosts your skill (AWS Lambda function)

1. user says the wake word "Alexa"
2. Alexa hears the wake word and then listens
3. Alexa captures the audio, and then sends it to the Alexa service
4. Alexa service uses the interaction model to figure out where to route the request
5. Alexa service sends a JSON request to the skill's Lambda function
6. The Lambda function inspects the JSON request
7. The Lambda function determines how to respond
8. The Lambda function sends a JSON response to the Alexa service
9. The Alexa service receive the JSON response, and then converts the output text into an audio file
10. The Alexa service sends the audio file to the Alexa-enabled device
11. alexa-enabled device receives the audio file and then plays the audio

## Steps to build a skill
1. design: design the voice interaction model of your skill
2. build: build the utternances, intents and slots in the Alexa developer console. The dev console saves your built interaction in JSON format, can edit the model with any editing tool. after have JSON interaction model ready, build the compute service Lambda function in the AWS Management Console

Select the programming language u want, the corresponding ASK software dev kit (SDK) and then begin coding your skill : Node.js, Python, and Java

Can build and host most skills for free with AWS Lambda, the service is free for the first 1 mil calls per month. u can provision your own Lambda endpoint or use an Alexa-hosted skill. With an alexa-hosted skill, alexa provisions the resources to run your skill for u without the need to create an AWS account

when the Lambda function is ready, integrate the Lambda function to your skill and then test it in the Alexa dev console. 

3. Test: alexa dev console has a built-in alexa simulator, which is similar to testing on an actual Alexa-enabled device

after testing your skill with the ALexa simulator, gather user feedback to resolve issues and make improvements before submitting yours skill for certification

4. Certify and publish
after beta testing, submit it for certification. After your skill passes certification, amazon publishes in the Alexa skills store for anyone to discover and use. Upon publication, u can promote ur skill to reach more customer



## Desing an engaging voice user interface

Voice design concepts: utterances, intents, and slots

a voice interaction model uses the following design concepts:

- Wake word (alexa): tell alexa to start listening to your commands
- Launch word : transitonal action word that signals the Alexa that a skill invocation will likely follows (tell, ask, open, launch, use)
- Invocation word: skill's invocation names
- Utterance: user's spoken request, can invoke a skill, provide inputs for skill, confim an action for alexa and so on. 
- Prompt: a string of context that u have alexa speak to user to ask for info
- Intent: represents an action that fulfill a user's spoken request. intents can optionally have arguments called slot
- slot value: input values provided in user's spoken request.

Dialog model is a structure that identifies the steps of a multi-turn conversation between your skill and the user.

## Voice interaction model

is a combinational of utterances, intents, and slots that u identify for your skill. to create an interaction model, define the requests and the words. ur lambda skill code then determines how your skill handles each intent. define the intents and utterenaces on paper and then iterate on those intents and utterances to try to cover as many possible ways the user can interact with the skill

then go to the alexa dev console and start to create the intents, utterances and slots. the console creates JSON code of your interaction model. u can also create the interaction model in JSON urself 

## voice design

to engage skill experience, u need to design your skill to mimic human conversation.

## visual design

the first alexa devices had a microphone and a speaker -> now devices with screens are a rapidly growing segment of Alexa use. multimodel skills based on Alexa Presentation Language (APL) have more than 3 times the amount of monthly active users, when compared to voice-only skills on multimodal devices. Skill that have APL have nearly double user engagement of voice-only skills on multimodal devices

## Situational design

voice-first method to design a VUI. u start with a simple dialog that helps keep the focus on the conversation. each interaction bw ur user and skill represents a turn. each turn has a situation that represnets the context. If it's the user's first time interacting with the skill, there is a set of data that is yet unknown. after the skill has stored the info, it will be able to use it the next time the user interacts with the skill

## Characteristics of a well-designed VUI  
- uses natural forms of communication
- navigates through info easily
- create an eyes-and-hands-free experience
- create a shared experience

## 5 best practices for voice design

1. stay close to Alexa's persona
2. write for the ear, then for the eye
3. be contextually relevant
4. be brief
5. write for engagement to increase retention

## Build a skill in 20 min

### How users will interact with Cake time

- make interaction bw your skill and user simple and natural.
    - ask user to guess celebrity birthday
    - determines if right or wrong
    - tell score and remember
    - greets returning users differently than new 1

- features:
    - utterances
    - intents
    - slots
    - dialog management
    - memory and persistence
    - customer profile settings

## Create the skill

- Step 1: create the skill
    - sign in
    - create your skill
    - change the skill invocation name

