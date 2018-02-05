# Yashu-Alexa-Skill

An Alexa skill to be used as a personal assistent.

## Request Flow
Here is the Alexa [Request Flow](./alexa-request-flow.JPG) for reference.

### Steps

1. Receive and send a voice request from Amazon echo or echo plus
2. Amazon Voice Service (AVS) receve the voice request and convert to text message
3. Send the Text message to identify the appropriate skill Alexa Skills Kit (ASK). This is done based on the Developer Tools to identify/process the Utterances, Intents and Slots
4. Construct the a request object based on the appropriate/identified Utterances, Intents and Slots 
5. Call the configured endpoint based on the constructed Request object
6. Process the request and send the response to AVS in SSML
7. Process the response and send to Amazon Echo in voice format

## Deploying locally

Make sure you have [Node.js](http://nodejs.org/) and the [Heroku Toolbelt](https://toolbelt.heroku.com/) installed.

```sh
git clone https://github.com/puttareddy/yashu-alexa-skill.git # or clone your own fork
cd yashu-alexa-skill
npm install
npm start
```

Your app should now be running on *[http://localhost:8080](http://localhost:8080)*.

For testing purposes, you can use either [ngrok](https://ngrok.com/download) or [localtunnel](https://github.com/alexa-js/alexa-home-server) before you deploy the app to any cloud hosted environments

### Testing it

You can access a test page to verify if the basic setup is working fine: *[http://localhost:8080/test](http://localhost:8080/test)*.

## Deploying to Heroku

```sh
heroku create
git push heroku master
heroku open
```

Alternatively, you can deploy your own copy of the app using this button:

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/alexa-js/alexa-app-example)

Your app should now be running on *https://`<app-name>`.herokuapp.com*, where `<app-name>` is the heroku app name.

### Testing it

You can access a test page to verify if the basic setup is working fine: *https://`<app-name>`.herokuapp.com/test*.

### References

This Alexa Skill is built using the [alexa-app](https://github.com/alexa-js/alexa-app) module with Express.