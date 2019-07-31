## Bolt app running on Cloud Functions for Firebase

This is a simple Bolt app which runs on Cloud Functions for Firebase.

* https://slack.dev/bolt/
* https://firebase.google.com/docs/functions

## Setup

Use node 10.x and its corresponding npm.

```
cp _firebaserc .firebaserc
vi .firebaserc # set your own project

npm install -g firebase-tools
firebase functions:config:set slack.signing_secret=522777abcabcabcabcabcabcabcabc
firebase functions:config:set slack.bot_token=xoxb-1234567890-123456789012-abcabcabcabcabcabc

cd functions
npm i
cd -
```

## How to run the app on your laptop

```bash
firebase serve
```

## How to deploy

```bash
firebase deploy
```

## How to configure Slack apps/GCP

### Slack App

https://api.slack.com/apps

Set `https://{your domain}.cloudfunctions.net/slack/events` as the Request URL for `/echo-from-firebase` slash command.

### Cloud Functions for Firebase

You have nothing to configure. Don't forget enabling the billing info if it's your first time to use it.

## How to make sure if it works

Use the command `/echo-from-firebase` in your Slack workspace.

## LICENSE  

The MIT License
