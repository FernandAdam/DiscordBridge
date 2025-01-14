# 🌉 Discord Bridge

A simple plugin providing a bridge between your discord and minecraft chats.

# Dependencies
- JDK >= 8
- Server implementing the Bukkit API (Spigot, Paper, ...)
- The jar Plugin to satisfy the dependencies: https://github.com/KettleMC-Network/Libraries/releases/tag/1.3.2

# 'Installation'
- clone the Repo
- add your bot token and the channel-id to the *Repo*/resources/config.json
- build the jar via gradle
- put the jar in your *Spigotserver*/plugins/ directory
- run the Server :)

# Important Files
- Main files:
    - src/net/kettlemc/discordbridge/*DiscordBridge.java*
        - *The main class of the plugin*
        - Function:
          - handle incoming Minecraft and Discord commands
          - setup config by methods from DiscordConfig.java
    - src/net/kettlemc/discordbridge/config/*DiscordConfig.java*
        - *Stores the config settings loaded from the "config.json"*
        - based on the configuration manager *Konfiguration*
        - Function:
          - defining methods to get the config values
    - src/net/kettlemc/discordbridge/discord/*DiscordBot.java*
        - *Wrapper class for the Discord bot itself*
        - Function:
          - simplifying the Discord API package functions (JDA)
          - defining methods for the DiscordBridge.java
    - src/net/kettlemc/discordbridge/discord/*command/\**
        - *Here are the discord commands the bot can handle*

