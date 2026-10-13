# Chat Interface Tool [force chat roblox.txt]

## Overview

A Roblox Lua utility that creates a chat interface GUI. When opened, it allows sending messages through the game's chat system, useful for testing chat filter behavior and message routing.

## Requirements

- Roblox game client
- Lua 5.1+ compatible runtime environment (Synapse X, Fluxus, KRNL, Electron)
- **Important:** Requires the game to expose its chat remote for this utility to work. Specifically:
  - An exposed `RemoteEvent` with no message source validation
  - The game must not validate message senders

## Setup

1. Install a compatible Roblox runtime environment.
2. Join a Roblox game with chat functionality.
3. Open your environment and paste the contents of `force chat roblox.txt`.
4. Execute the utility.
5. The utility creates an `AdvancedChatGui` ScreenGui in `CoreGui` (or `PlayerGui` if `CoreGui` is not accessible).

## How It Works

1. The utility creates a `ScreenGui` named `AdvancedChatGui` and destroys any existing instance with the same name.
2. A chat GUI is built that mimics the native Roblox chat interface.
3. When the user sends a message through the chat, it fires the game's chat `RemoteEvent` with the message content.
4. If the remote accepts messages without sender validation, the message will appear in-game.

## Usage

- Type messages in the chat box and press Enter.
- Messages will be sent through the game's chat RemoteEvents.
- If the game validates message sources, the messages will be filtered or rejected.

## Tutorial

Watch full setup and usage examples on YouTube:
https://www.youtube.com/@kydn-iu5kd

## Disclaimer

For educational purposes only. This utility demonstrates the importance of client-server validation. Many modern games properly validate message sources, so this technique may not work in most places.