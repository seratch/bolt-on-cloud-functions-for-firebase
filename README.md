## Bolt app running on Cloud Functions for Firebase

## Setup

Use node 10.x and its corresponding npm.

```
npm install -g firebase-tools
cd functions
npm i
cp -p _config.js config.js # and modify config.js
cd -
```

## How to run the app

```bash
firebase serve
```

## How to deploy

```bash
firebase deploy
```

## How to configure

### Slack App Configuration

Set `https://{your domain}.cloudfunctions.net/slack/events` as the Request URL for event subscriptions.

### Cloud Functions for Firebase

You have nothing to configure. Don't forget enabling billing infor if it's your first time to use it.

## Make sure if it works

Post a message including `hello`. Then you'll receive a message saying `Hey there @yourname` from the bot user!

## LICENSE  

The MIT License