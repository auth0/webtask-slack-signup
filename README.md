Create Slack signup page using Auth0 webtasks
======

![image](https://cloud.githubusercontent.com/assets/3391028/20866792/4f930b42-ba14-11e6-94fc-18b1c7578137.png)


With [Auth0 Webtasks](https://webtask.io) you can quickly create a signup page for your Slack team without worrying about hosting, backends, and devops. 

Follow these 3 steps:

```bash
npm install -g wt-cli
wt init
wt create https://raw.githubusercontent.com/auth0/webtask-slack-signup/master/slack-invite.js \
    --name {your_slack_team}-signup \
    --capture \
    --parse-body \
    --secret SLACK_ORG={your_slack_team} \
    --secret SLACK_TOKEN={your_slack_admin_token}
```

The `{your_slack_admin_token}` can be obtained from Slack [here](https://api.slack.com/docs/oauth-test-tokens). 

Optionally, you can also provide `--secret LOGO_URL={url_to_your_logo}` which will display your custom logo on the signup page. It should be square and not less than 100x100px. 

Use the resulting URL as your Slack signup page. Enjoy!
