webtask-slack-signup: Create Slack signup page using Auth0 webtasks
======

With [Auth0 Webtasks](https://webtask.io) you can quickly create a signup page for your Slack team without worrying about hosting, backends, and devops. 

Follow these 3 steps:

```bash
npm install -g wt-cli
wt init
wt create https://raw.githubusercontent.com/auth0/webtask-slack-signup/master/slack-invite.js \
    --name {your_slack_team}-signup \
    --capture \
    --secret SLACK_ORG={your_slack_team} \
    --secret SLACK_TOKEN={your_slack_admin_token}
```

Use the resulting URL as your Slack signup page. Enjoy!
