# remind-me

A command-line reminder tool that supports natural language dates and times, inspired by Slack's `/remind` feature.

```
$ remind me to go outside for some fresh air in five minutes
# Ok, I'll remind you to "go outside for some fresh air" on Sunday, September 20 at 4:05 pm
```

## Installation

This module uses some newer JavaScript features, so you'll need iojs or node >=4 installed to use it.

It has been tested on Mac OS X Yosemite, but should work on any system with `cron` support.

```sh
npm i -g remind-me && remind
```

## Usage

**remind me**

Create a reminder.

```
remind me in two hours to take a break
remind me to do some deep breathing in 10 minutes
remind me at 3pm to wash the dishes
remind me to wash the dishes at 4:00 pm tomorrow
remind me to get out of bed tomorrow
remind me to put on pants at 8:36 am tomorrow
remind me on friday at 9pm to go party
remind me on February 2 at 6:30am to look for my shadow
```

#### remind list

List all upcoming reminders and their times

#### remind edit

Open `~/.remind-me/reminders.json` in your `$EDITOR`

#### remind config

Open `~/.remind-me/config.json` in your `$EDITOR`

## Notifiers

The following notifiers are supported. To enable or disable any of them, type `remind config`.

#### `say`

The Mac OS X [say](http://www.maclife.com/article/columns/terminal_101_making_your_mac_talk_%E2%80%9Csay%E2%80%9D) command is enabled by default. This reads your reminder aloud in a computer voice. You can customize the voice. The full list is available by typing `say -v "?"` in your terminal.

Enabled by default.

#### Desktop Notifications

This display reminders using your OS's built-in notification system. This notifier uses the popular and well-maintained [node-notifier](https://github.com/mikaelbr/node-notifier#readme) module.

Enabled by default.

#### Text Messages with Twilio

Send reminders to your phone as text messages using Twilio. You can sign up for a free account which will work but prepends a nag message to all your texts, or you can pay for texts for a nominal fee. To find your Twilio phone number, visit  https://www.twilio.com/user/account/phone-numbers/incoming. To find your Twilio SID and token, visit https://www.twilio.com/user/account/settings

#### Slack

Send messages to a Slack channel. Uses the [node-slack](https://github.com/xoxco/node-slack) module.

Disabled by default. Requires configuration.

## Tests

```sh
npm install
npm test
```

## Dependencies

- [chrono-node](https://github.com/berryboy/chrono): A natural language date parser in Javascript
- [cp](https://github.com/stephenmathieson/node-cp): cp for node
- [crontab](https://github.com/dachev/node-crontab): A module for reading, creating, deleting, manipulating, and saving system cronjobs with node.js
- [dateparser](https://github.com/jhaynie/dateparser): A human language relative date parser
- [easypattern](https://github.com/nadav-dav/EasyPattern): EasyPattern is a readable alternative to regular expressions
- [mkdirp](https://github.com/substack/node-mkdirp): Recursively mkdir, like `mkdir -p`
- [node-notifier](https://github.com/mikaelbr/node-notifier): A Node.js module for sending notifications on native Mac, Windows (post and pre 8) and Linux (or Growl as fallback)
- [node-slack](https://github.com/xoxco/node-slack): Send and receive Slack Webhooks easily!
- [prettydate](https://github.com/bluesmoon/node-prettydate): Format dates nicely
- [require-dir](https://github.com/aseemk/requireDir): Helper to require() directories.
- [rimraf](https://github.com/isaacs/rimraf): A deep deletion module for node (like `rm -rf`)
- [tmp](https://github.com/raszi/node-tmp): Temporary file and directory creator
- [twilio](https://github.com/git+https:/): A Twilio helper library
- [user-home](https://github.com/git+https:/): Get the path to the user home directory
- [uuid](https://github.com/shtylman/node-uuid): Rigorous implementation of RFC4122 (v1 and v4) UUIDs.

## Dev Dependencies

- [mocha](https://github.com/mochajs/mocha): simple, flexible, fun test framework
- [standard](https://github.com/feross/standard): JavaScript Standard Style

## License

ISC

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
