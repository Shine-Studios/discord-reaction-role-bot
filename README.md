# Discord Reaction Role Bot

A Discord bot that allows users to self-assign roles using reactions.

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/discord-reaction-role-bot/master/assets/isUnique.gif" />
</div>

## Setup

1. Adapt and follow the steps found in [create-discord-bot](https://github.com/peterthehan/create-discord-bot).

> Don't forget to give your bot the `Manage Roles` permission!

2. Navigate to [src/config.js](https://github.com/peterthehan/discord-reaction-role-bot/blob/master/src/config.js) and add your own emoji-role rules:

```js
models: {
  'MESSAGE_ID': {
    channelId: 'CHANNEL_ID',
    isUnique: true,
    emojiRoleMap: {
      'EMOJI_1': ['ROLE_1_ID'],
      'EMOJI_2': ['ROLE_2_ID'],
      'EMOJI_3': ['ROLE_3_ID', 'ROLE_4_ID']
    }
  },
  // ...Add as many rules as you want.
}
```

> If `isUnique` is true, the user can select only one role group at a time (gif above).

> If `isUnique` is false, the user can select as many role groups as they want.

> An emoji can map to multiple roles (as seen in `EMOJI_3`).
