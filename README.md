# 2017 Conversation Robot - Roomba meets Watson - Hear the voice of AI 
Transforming the lightweight IoT with Voice UI, Java, AI, and Cloud

[This repository is an extension for the Massive Online Open Course - Robots are coming! Build IoT apps with IBM Watson, Swift, and Node-RED](http://ibm.biz/watson-roomba-2017)

This repository demonstorates steps needed to add Conversation and Voice UI IBM Watson services to IoT & mobile solution:

## 1. Conversation service
This step shows adding the java based conversation UI on an Android (or iOS) device

- First open a [IBM Cloud - Bluemix](http://bluemix.net) console and from the menu "hamburger" on the left choose Mobile. 
- It will open mobile projects - choose "conversation". 
- Download the mobile project for Android (or iOS), 
- and using Android Studio (or Xcode for iOS) finish the deployment. 
- In the step of creating the DIALOG please use the attached ```watson-bot-conversation.json```, and upload it to the conversation service.
- check if your application binds with the conversation service - ask: "who are you?", or request: "tell me a joke".

## 2. IoT with the Voice UI
This step shows deploying Speech to Text, Conversation, and Text to Speech Services on Rapsberry Pi.

- Start by forking the repo of TJBot: https://github.com/ibmtjbot/tjbot/tree/master/recipes/conversation;
- Create and add Speech to Text and Text to Speech Watson services (available on IBM Cloud - Bluemix for all except Lite accounts);
- when all the credentials are entered into the credentials.js,
```
$ cd ../recipes/conversation
$ npm install

$ cp config.default.js config.js
$ nano config.js
<enter your credentials and the conversation workspace ID in the specified places>
```

Run!
```
$ sudo node conversation.js
```

An attention word is used so TJBot knows you are talking to him. The default attention word is 'Watson', but you can change it in conversation.js as follows. Update conversation.js and change tjConfig to add the 'robot' section:
```javascript
// turn on debug logging to the console
var tjConfig = {
    verboseLogging: true,
    robot: {
        name: 'Watson',
        gender: 'male'
    }
};
```
You can change the 'name' to whatever you would like to call your TJBot. In addition, if you change the gender to 'female', TJBot will use a female voice to speak to you!

## 3. Invoking some actions with IoT Platform
This step shows how to bind together IoT and cloud for data collection and AI based analysis

Follow the github description on deploying the app: https://github.com/blumareks/iot-watson-swift/tree/master/lab2

references:
- http://www.instructables.com/id/Build-a-Talking-Robot-With-Watson-and-Raspberry-Pi/
- https://github.com/ibmtjbot/tjbot/tree/master/recipes/conversation
