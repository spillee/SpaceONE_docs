---
title: "Slack Protocol"
linkTitle: "Slack Protocol"
weight: 4
date: 2021-08-13
description: >
    Notification Plugin Slack Protocol Configuration Guide
---

## Overview
We can also add **`Slack`** to our list of `Notification` channels. There are few prerequisites to use Slack Bot on SpaceONE notification service, and the following will guide you to your **SpaceONE** notification journey with your **`Slack`** workspace. 

## Prerequisites
Install the Slack app on your phone or PC. You will need a **OAuth Token** and **channel**. 

### How to get Slack OAuth Token
Open the   `Slack App Directory` of your Slack workspace. 
`Slack OAuth Token` is generated by creating a `slack app` and a `bot user`. <br>
Slack OAuth token gives you the ability to handle things that relate to your app as a whole. To generate `Slack Access Token`, Follow the steps above: <br>
1. Visit [here](https://api.slack.com/apps) and create a new slack app. Fill out your App Name and select the development workspace where you'll play around and build your app.
2. `OAuth & Permissions` section shows the information of tokens which allow your slack app to use features that apply to SpaceONE notification events. Copy the Token information in somewhere. <br>
![slack_copy_app_token.png](/ko/docs/guides_v1/alert_manager/notification/notification_img/slack_copy_app_token.png)
3. Go to `Scopes` section, you can add permission to access to slack channel. Click on 'Add an OAuth Scope' and select `chat:write` scope.
![slack_bot_token_scope.png](/ko/docs/guides_v1/alert_manager/notification/notification_img/slack_bot_token_scope.png)
3. Go to `Basic Information` section, you can install your app by click on `Install to Workspace` button.  

{{% alert title="Token Information Alert" %}}
Token information need to be considered secure. Be sure not to share token
{{% /alert %}}

### Display setting of SpaceONE Slackbot
Add Display settings to make your SpaceONE Slackbot even better.

1. Visit [API Slack App](https://api.slack.com/apps) and select your SpaceONE slack app. 
2. Select the `Basic Information` in on the left menu and Find the `Display Information` section.
3. Fill out the App name and Short description.
4. Upload SpaceONE Slackbot icon on the `App icon & Preview`. Download the Bot image [here](https://spaceone-custom-assets.s3.ap-northeast-2.amazonaws.com/console-assets/icons/spaceone_slackbot_icon.png).

### How to generate Slack Bot users
Bot users are automated user accounts you can message with directly. You can eventually receive notification messages by inviting Bot User in your channel. 
<br>
1. Go back to your slack workspace console. 
2. Head to  `Manage apps` page by click on `your_workspace_name` on the top-left corner > `Administration` > `Manage apps`
3. On the `Bot User` section, generate the Bot User and give it a name!
4. Go back to your slack workspace console again, and invite the bot by following steps:
    - Go to the channel
    - Click the channel's name, go to `Integrations`, and click `Add apps`.
    - Find the apps we created right before, and add it.
    - Then, click `Add this app` button to a channel.

## Add Slack Channel to your Project / User in SpaceONE
Go to `SpaceONE Console` > `Project` which you want to get alerts through Slack.

### Basic Information
![telegram_spaceone_console.png](/ko/docs/guides_v1/alert_manager/notification/notification_img/telegram_spaceone_consol.png)
Set information above.<br>
These items below are descriptions for plugins
![slack_add_info.png](/ko/docs/guides_v1/alert_manager/notification/notification_img/slack_add_info.png)

|Item|Descriptions|
|:--:|:--|
|Channel Name|Notification channel name|
|Notifications Level|Which level to be placed in escalation policy, see [Escalation Policy for details](/docs/guides_v1/alert_manager/escalation_policy/)|
|Slack Channel|Name of the slack channel to publish message. No need `#` in front of channel name|
|Slack Token|Token of slack app|

Save and Test, now you are ready for SpaceONE Journey with Slack notification channel.

### Notification Schedule
You can select when to receive alarm. There two options
![Notification Schedule](/ko/docs/guides_v1/alert_manager/notification/notification_img/notification_img_01.png)

|Setting Mode|Descriptions|
|:--:|:--|
|All Time|Receive alert notification any time|
|Custom|Receive alert notification within designated time period|

### Topic
Notification subscribes topics to check which alarm to send

{{% alert title="About Notification Topics" %}}
Now only monitoring.Alert topics are available. Other topics will be created in future release.
Just pin _**Setting Mode**_ to _**Receive all notifications**_
{{% /alert %}}

|Setting Mode|Descriptions|
|:--|:--|
|Receive all notifications|Allow notification channel to send all alert messages from _**any topics**_|
|Receive notifications based on selected topics|Allow notification channel to send alert message from _**selected topics**_|

## Troubleshooting
Visit [Slack Basic App Setup](https://api.slack.com/authentication/basics#installing) for an additional explains of new Slack app.<br>
`Happy SpaceONE-ing with Slack notification channel!`