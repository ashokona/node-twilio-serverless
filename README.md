
## Setup

1. Sign up for a [Twilio account](http://www.twilio.com)

2. Create a [new phone number](https://www.twilio.com/console/phone-numbers/) in your Twilio trial account

3. Grab your ACCOUNT SID and AUTH TOKEN from the [Twilio console](https://www.twilio.com/console) and plug those into the `serverless.yml` file in the next step

4. Set your `env` variables in `serverless.yml` with your Twilio account values

  ```yml
  environment:
    # replace these env variables with your twilio account values
    TWILIO_ACCOUNT_SID: YOUR-TWILIO-ACCOUNT-SID-HERE
    TWILIO_AUTH_TOKEN: YOUR-TWILIO-AUTH-TOKEN-HERE
    TWILIO_PHONE_NUMBER: YOUR-TWILIO-PHONE-NUMBER-HERE
  ```

5. Deploy and Invoke the function and send an SMS message

  Update the `to` phone number the `event.json` file and `message` to send in the SMS

  Then invoke the function with the serverless CLI. Set the `--path event.json` so the function knows where to send the SMS.

  You need to install and configure aws-cli in order to deploy

  ```bash
  serverless deploy
  serverless invoke -f sendText --path event.json
  ```
