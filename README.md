# Slackify-Markdown

Slackify-Markdown is a Markdown to [Slack-specific-markdown](https://api.slack.com/docs/message-formatting#message_formatting) converter, based on [Unified](https://github.com/unifiedjs/unified) and [Remark](https://github.com/remarkjs/remark/).

## Install

```bash
npm install slackify-markdown
```

## Usage

```js
const slackifyMarkdown = require('slackify-markdown');
const markdown = `
# List of items

* item 1
* item 2
* item 3
`;

const slackMarkdown = slackifyMarkdown(markdown);
```

#### Emojis
Emojis map can be passed through options to replace some specific emoji codes

```js
const options = {
  emojis: { ':hello:': ':bye:' }
};

slackifyMarkdown(':hello: my fried!', options); // -> ':bye: my friend!'
```

### Copyright and License

Copyright Yevhenii Baraniuk, 2018

[MIT Licence](LICENSE)
