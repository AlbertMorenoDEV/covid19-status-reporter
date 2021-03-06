# COVID-19 Status Reporter
Send a report to slack channel or user with the latest status updates about COVID-19 on each country

> COVID19-status-reporter requires [Node.js](https://nodejs.org/en/) version 9 or above

## How it works

1. Run `yarn install` to download the dependencies.
2. Then create a `.env` file with the environment variables that are needed for the service. You can copy/paste the `.env.example` file and change the values:

    - **SLACK_API_TOKEN**: The slack token that you can get once you [create a slack application](https://api.slack.com/apps) under the **OAuth & Permissions** menu.
    - **SLACK_CHANNEL**: The channel's or user's ID (the one that is gonna receive the message)
    - **CRON_PATTERN**: Cron expression, for example, this pattern `*/5 *  * * *` is gonna send a message every 5 seconds. You can learn more about cron [here](https://opensource.com/article/17/11/how-use-cron-linux)
    - **PORT**: The port where the application is gonna run
    - **TIMEZONE**: To let the cronjob knows which timezone is gonna use. You can get the timezone values from [here](https://momentjs.com/timezone/)
3. Run `yarn build` so that to create the production bundle inside the build folder.
4. Start up the server, I recommend [PM2](https://pm2.keymetrics.io/) (`pm2 start build/index.js`) but you can use your favourite one ;)

## Upcoming features

- [ ] Add unit tests (yes, I know! I have should done it before!...shame on me...)
- [ ] Dockerize the application
- [ ] Add Telegram service
- [ ] Add log file system

## LICENSE
MIT. See [LICENSE](https://github.com/gusbueno/covid19-status-reporter/blob/master/LICENSE) for more details.
