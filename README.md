# 2017-javaone
Transforming the lightweight IoT with Voice UI, Java, AI, and Cloud

[This repository is an extension for the Massive Online Open Course - Robots are coming! Build IoT apps with IBM Watson, Swift, and Node-RED](https://github.com/blumareks/2017-javaone/blob/master/README.md)

This repository demonstorates steps needed to add Conversation and Voice UI IBM Watson services to IoT & mobile solution:

## 1. Conversation service
This step shows adding the java based conversation UI on an Android (or iOS) device

- First open a [IBM Cloud - Bluemix](http://bluemix.net) console and from the menu "hamburger" on the left choose Mobile. 
- It will open mobile projects - choose "conversation". 
- Download the mobile project for Android (or iOS), 
- and using Android Studio (or Xcode for iOS) finish the deployment. 
- In the step of creating the DIALOG please use the attached ```watson_bot_dialog.json```, and upload it to the conversation service.
- check if your application binds with the conversation service - ask: "who are you?", or request: "tell me a joke".

## 2. IoT with the Voice UI
This step shows deploying Speech to Text, Conversation, and Text to Speech Services on Rapsberry Pi

## 3. Invoking some actions with IoT Platform
This step shows how to bind together IoT and cloud for data collection and AI based analysis


references:
- http://www.instructables.com/id/Build-a-Talking-Robot-With-Watson-and-Raspberry-Pi/
- https://github.com/ibmtjbot/tjbot/tree/master/recipes/conversation
