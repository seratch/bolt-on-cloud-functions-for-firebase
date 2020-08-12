## Bolt app running on Cloud Functions for Firebase

This is a simple Bolt app which runs on Cloud Functions for Firebase.

* https://slack.dev/bolt-js/
* https://firebase.google.com/docs/functions

## Setup

Use node 12.x and its corresponding npm.

```bash
cp _firebaserc .firebaserc
vi .firebaserc # set your own project

npm install -g firebase-tools
firebase login
firebase functions:config:set slack.signing_secret=xxx
firebase functions:config:set slack.bot_token=xoxb-111-111-xxx
```

## How to run the app on your laptop

```bash
cd functions
npm i
cd -
firebase functions:config:get > .runtimeconfig.json
firebase serve
```

## How to deploy

```bash
firebase deploy
```

## How to configure Slack apps/Firebase

### Slack App

https://api.slack.com/apps

* Set `https://{your domain}.cloudfunctions.net/slack/events` as the Request URL for `/echo-from-firebase` slash command.
* Add `commands`, `chat:write` scopes
* Install the app to your development workspace

### Cloud Functions for Firebase

You have nothing to configure. Don't forget enabling the billing info if it's your first time to use it.

## How to make sure if it works

* Go the development Slack workspace
* Invite the bot user to a channel
* Run `/echo-from-firebase` in the channel
* Verify the bot replies to you - You said "xxx"

## LICENSE  

The MIT License
