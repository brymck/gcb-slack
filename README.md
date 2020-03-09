# gcb-slack

![Build](https://github.com/brymck/gcb-slack/workflows/Build/badge.svg)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

Google Cloud Build webhook for Slack, mostly taken from  
https://cloud.google.com/cloud-build/docs/configure-third-party-notifications#writing_the_cloud_function

## Usage

Clone this repo:

```bash
git clone git@github.com:brymck/gcb-slack.git
cd gcb-slack
```

Then follow the instructions in  
https://cloud.google.com/cloud-build/docs/configure-third-party-notifications  
skipping over the "Writing the Cloud Function" instructions.

You can also fork this repo, create the following secrets in GitHub, and have the function deployed automatically on commits to master via GitHub Actions:

- `PROJECT_ID` - The name of your Google Cloud project
- `SA_EMAIL` - The email of the service account deploying this function. Ensure your service account has the `Cloud Functions Admin` role.
- `GOOGLE_APPLICATION_CREDENTIALS` - Base64-encoded credentials for the service account
- `SLACK_WEBHOOK_URL` - The webhook URL generated when creating a new app in Slack per the instructions [here](https://cloud.google.com/cloud-build/docs/configure-third-party-notifications#preparing_the_slack_application)
