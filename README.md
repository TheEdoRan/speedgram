# Speedgram

Execute a speedtest and send the result to a user via Telegram bot.

## Requirements

cURL and [Speedtest CLI](https://www.speedtest.net/apps/cli).

### Steps

1. Choose a Speedtest.net server with [@speedtestidbot](https://telegram.me/speedtestidbot)
2. Create a new Telegram bot with [@BotFather](https://telegram.me/botfather)
3. Get your Telegram user ID with [@myidbot](https://telegram.me/myidbot)

⚠️  **Don't forget to start the chat with your newly created bot, otherwise it cannot send messages to you!**

## Installation

Clone this repository and `cd` into the created directory.

If you prefer to access this script globally in the system, you can add it to your `$PATH`, by copying it to something like `/usr/local/bin`.

## Usage

```bash
Execute a speedtest and send the result to a user via Telegram bot.

Usage: speedgram [-h] -s -b -u
Options:
  h    Print this help.
  s    Server ID. Choose a server with @speedtestidbot.
  b    Bot token. Create a bot with @BotFather.
  u    User ID. Get yours with @myidbot.
```

Example:

```bash
./speedgram -s 47747 -b 123456:ABCDEF1234ghIkl_zyx57W2v1u123ew11 -u 123456

#-s: server ID (requirements/step 1)
#-b: bot token (requirements/step 2)
#-u: user ID (requirements/step 3)
```

## Cronjob

If you want to execute this script automagically, repeatedly, and headlessly:

1. Open the crontab file with your preferred editor: `crontab -e`
2. At the end of it, create the new cronjob. For example, this one below executes the script every day, every hour at minute 0. You can also use [crontab.guru](https://crontab.guru/) to generate it.

```bash
0 * * * * /path/to/script/speedgram -s <server_id> -b <bot_token> -u <user_id>
```

## License

This project is published under the [MIT License](https://opensource.org/licenses/MIT).
