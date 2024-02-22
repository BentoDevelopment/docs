---
title: Pronouns4j Documentation
subtitle: Documentation and wiki for Pronouns4j
authors:
  - phpfpm
description: The documentation and wiki for Pronouns4j
icon: octicons/hash-16
status: new
---

# Pronouns4j Documentation

Pronouns4j is a Minecraft plugin designed to revolutionize and diversify your Minecraft server experience by allowing users to specify their preferred pronouns. Server admins can integrate Pronouns4j into their server setup to ensure messages and interactions reflect the chosen pronouns of players.

## Overview

Pronouns4j introduces a set of placeholders and commands that enable users to set, view, and clear their pronouns. Additionally, it provides support for integrating with other plugins such as EssentialsX chat to ensure proper recognition and usage of pronouns in in-game messages.

### Product Information

- **Product Name:** Pronouns4j
- **Description:** Revolutionize and diversify your Minecraft server with Pronouns4j.
- **Download:** Coming soon..

## Installation and Setup

### Prerequisites

Before installing Pronouns4j, ensure that your Minecraft server meets the following requirements:

- **Minecraft Server:** Version 1.20.1 or higher
- **PlaceholderAPI**
- **EssentialsX Chat:** (Optional) If integrating with EssentialsX chat, ensure it is installed and configured.

### Installation

1. Download the Pronouns4j plugin JAR file from [here](#).

2. Place the downloaded JAR file into the `plugins` directory of your Minecraft server.

3. Restart your server to enable the plugin.

### Configuration

Pronouns4j offers a configuration file that allows you to customize certain settings. To access the configuration file, follow these steps:

1. Navigate to the `plugins/Pronouns4j` directory in your server files.

2. Open the `config.yml` file using a text editor.

3. Modify the configuration settings as needed. Below is an example configuration:

```yaml
sql: # (1)
  enabled: false
  host: localhost
  port: 3306
  username: root
  password: root
  database: default
metrics: true # (2)
```

1. `false` - Pronouns4j will use a local database stored in the plugin's data folder.  
`true` - Pronouns4j will use the database provided in the configuration.
2. This is for bStats analytics. This helps us track certain stats for the use of our plugin (game version, system architecture, server location etc.)

## Usage

### Setting Pronouns

Players can set their preferred pronouns using the following command:

```
/pronouns set <subjective> <objective> <possessive> <reflexive>
```

Replace `<>` with your preferred pronouns.

### Viewing Pronouns

To view your currently set pronouns, use the following command:

```
/pronouns view
```

### Clearing Pronouns

If you wish to clear your pronouns and revert to the default, use the following command:

```
/pronouns clear
```
## Placeholders

Pronouns4j provides the following placeholders:

- `%pronouns4j_subjective%`: Shows the subjective pronoun (e.g., He)
- `%pronouns4j_objective%`: Shows the objective pronoun (e.g., Him)
- `%pronouns4j_possessive%`: Shows the possessive pronoun (e.g., His)
- `%pronouns4j_reflexive%`: Shows the reflexive pronoun (e.g., Himself)
- `%pronouns4j_pronouns%`: Shows the basic pronouns (e.g., He/Him/His)

You can manipulate these placeholders by adding "_upper" to make them capitalized or "_capital" to make the first letter of the pronoun capitalized.

### Integrating with EssentialsX Chat
!!! warning

    To ensure proper recognition of pronouns in in-game messages through EssentialsX chat, you need to use specific placeholders. Add the following placeholders to your EssentialsX chat configuration:
    
    ```yaml
    <pronouns_sub> - For the subjective pronoun (e.g., He, She, They)
    <pronouns_obj> - For the objective pronoun (e.g., Him, Her, Them)
    ```  
    !!! example

        ```yaml title="Example"
        format: '[<pronouns_sub>/<pronouns_obj>] {DISPLAYNAME} {MESSAGE}'
        ```
    
        It is essential to configure these placeholders correctly to ensure seamless integration with Pronouns4j.


## Additional Resources

For more information and support, refer to the following resources:

- [Pronouns4j Discord](https://discord.gg/gNTPAsJRZt)
- [Pronouns4j Wiki](https://bentodevelopment.github.io/docs/)
- [EssentialsX Chat Documentation](https://essentialsx.net/wiki/Home.html)
