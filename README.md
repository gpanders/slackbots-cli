# slackbots-cli

## Usage

    npm install
    ./slackbots --bot <botname> --channel <channel>

Where `<botname>` is the name of a bot that has a corresponding 
file in your bots directory (`bots/` by default).

This will open up an interactive terminal, where each message you
send will send a message from your bot to the channel you specify. Use
`!help` from within the slackbots terminal to get a list of available
commands.

A bot config file needs only 2 attributes: a `name` and *either* `icon_url` OR `icon_emoji`.
Use `_template.json` as a starting point.


Example:

*bots/ghost.json*

    {
        "name": "Ghost Bot",
        "icon_emoji": ":ghost:"
    }

`./slackbots --bot ghost --channel general`

Get your Slack API web token from [here](https://api.slack.com/docs/oauth-test-tokens)
and put it in `config.json`.
