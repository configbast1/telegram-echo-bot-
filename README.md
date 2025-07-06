# 🤖 Java Telegram Echo Bot

This repository contains a simple **Telegram Echo Bot** written in **Java** using the [TelegramBots](https://github.com/rubenlagus/TelegramBots) library.  
The bot receives any text message and sends back the same message prefixed with `"Echo:"`.

This project is a good starting point if you want to learn:
- How to connect your Java application to the Telegram Bot API.
- How to structure a simple bot project using Maven.
- How to handle incoming updates and send replies.

---

## ✨ **How it works**

The core logic is implemented in two files:
- [`EchoBot.java`](src/main/java/com/example/bot/EchoBot.java): contains the bot logic. It implements `TelegramLongPollingBot` and overrides `onUpdateReceived()` to process incoming messages.
- [`Main.java`](src/main/java/com/example/bot/Main.java): entry point that registers your bot with the Telegram API.

All configuration for dependencies and build steps is managed by [`pom.xml`](pom.xml).

Before running, make sure you have created your own bot with [@BotFather](https://t.me/botfather) and replaced `YOUR_BOT_USERNAME` and `YOUR_BOT_TOKEN` in `EchoBot.java`.

---

## 🗂️ **Key files and folders**

- [src/main/java/com/example/bot/](src/main/java/com/example/bot/) — Java source files.
- [EchoBot.java](src/main/java/com/example/bot/EchoBot.java) — main bot logic.
- [Main.java](src/main/java/com/example/bot/Main.java) — starts your bot.
- [pom.xml](pom.xml) — Maven project config.
- [.gitignore](.gitignore) — standard Java ignore rules.
- [README.md](README.md) — this file.

---

## 🚀 **How to run**

1. Create your bot via [@BotFather](https://t.me/botfather) and get your token.
2. Replace the placeholders in [`EchoBot.java`](src/main/java/com/example/bot/EchoBot.java).
3. Make sure you have [Java 17+](https://adoptopenjdk.net/) and [Maven](https://maven.apache.org/) installed.
4. Build and run your bot:
   ```bash
   mvn clean install
   mvn exec:java
