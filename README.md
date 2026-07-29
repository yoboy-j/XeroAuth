# XeroAuth

A secure authentication plugin rebuilt from the ground up for Paper servers

## Index

- [What It Does](#what-it-does)
- [Features](#features)
- [Installation](#installation)
- [Commands](#commands)
- [Permissions](#permissions)
- [Configuration](#configuration)
- [How It Works](#how-it-works)
- [Compatibility](#compatibility)
- [Support](#support)

## What It Does

Keeps your server safe from cracked accounts and bots

When a player joins they get frozen on an invisible barrier platform at spawn and they have to verify before they can do anything

## Features

- Register and login with passwords
- Map captcha that stops bots and alt accounts
- Rejects weak passwords like password 1234 and admin
- Locks accounts temporarily after too many failed attempts
- Invisible barrier platform instead of ugly bedrock blocks
- Freeze that works without paper fly kick errors
- Platform stays on disconnect and reapplies on rejoin
- SQLite database no mysql setup needed
- Configurable messages sounds and fireworks
- PlaceholderAPI support

## Installation

1. Download the latest jar from Releases
2. Drop it into your plugins folder
3. Restart the server
4. Edit the config to your liking

## Commands

- `/register <password> <password>` - create an account
- `/login <password>` - verify your account
- `/auth force login <player>` - force login a player
- `/auth force unregister <player>` - force unregister a player
- `/auth set register <player> <password>` - set password for a player
- `/auth set login <player> <password>` - set login for a player
- `/auth reload` - reload configuration
- `/auth setspawn` - set auth spawn location

## Permissions

- `xeroauth.admin` - full admin access
- default - register and login

## Configuration

```yaml
spawn:
  world: "world"
  x: 0
  y: 0
  z: 0

auth-timeout: 120

captcha:
  enabled: true
  length: 6

login:
  max-attempts: 5
  lockout-duration: 300

register:
  min-password-length: 4
  max-password-length: 32
```

## How It Works

1. Player joins and gets frozen on a barrier platform at spawn
2. New players get a map with a code in their offhand
3. They type the code in chat then register with a password
4. Returning players just type their password to login
5. Once verified the platform disappears and they can play

## Compatibility

- Paper 1.21.11
- Java 21
- SQLite with no external dependencies
- PlaceholderAPI support included

## Support

- Join the Discord for help and updates - https://discord.gg/mDfh3VrxD
- Report bugs in the bug reports channel with your server version and error logs
- Suggest features in the suggestions channel
- Share your setup and configs in the showcase channel
- Star the repo if you like it
  
## Credits

©2026 Xero
