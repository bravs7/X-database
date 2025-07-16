# League of Legends Skins for Developer Repository

This repository aims to provide a centralized and easily accessible location for all in-game skins available for League of Legends. The purpose of this project is not to undermine the custom skin scene within League of Legends.

Using custom skins does not confer any competitive advantage, as they are only visible to the player utilizing them. 

## Repository Structure

The repository is organized as follows:

```
/
├── 1/  # Annie
│   ├── 0.fantome  # Default skin
│   ├── 1.fantome 
│   ├── 2.fantome
│   └── ...
├── 2/  # Olaf
│   ├── 0.fantome # Default skin
│   ├── 1.fantome
│   └── ...
└── README.md
```


Key points to remember:

1. The .fantome file is a renamed ZIP archive with a specific internal structure.
2. It must contain the standard folders: RAW (for legacy content), WAD (for main mod files), and META (for metadata).
3. The WAD folder should mirror League of Legends' file structure precisely for proper mod installation.
4. The META folder must include an info.json file with basic mod information such as name, author, and version.
5. Modern mods should primarily use the WAD folder structure for optimal performance and file size.
6. The RAW folder is mainly for backwards compatibility and should be avoided for new mods unless absolutely necessary.


## API Endpoints

To get champion and skin names, you can use the following Data Dragon API endpoints:

1. Champion Data:
   ```
   https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champion-summary.json
   ```

2. Skins and chromas ID for a Specific Champion:
   ```
   "https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champions/{champion_id}.json"
   ```
  

## Disclaimer

This project is not endorsed by Riot Games and does not reflect the views or opinions of Riot Games or any of its affiliates. League of Legends and all related properties are trademarks or registered trademarks of Riot Games, Inc.

The use of these assets for skin hack development may violate Riot Games' terms of service. Use at your own risk.

This repository is not affiliated with the moderators of r/LoLCustom.


Consider developing or using a tool that:
1. Reads the .fantome files from this repository
2. Makes minor, non-functional alterations to the file content (e.g., adding benign metadata or comments)
3. Generates a new file with a different hash but identical functionality

By implementing such a system, you can help protect users of your development from potential bans or other consequences, should Riot Games decide to take action against the use of these specific file hashes. Remember, the goal is to preserve functionality while avoiding direct matches to the files in this public repository.

Please note that while this method may reduce the risk of detection via hash matching, it does not guarantee protection against all forms of detection or potential consequences of using custom skins. Always inform your users about the risks involved in using custom skins or any modifications to the game client.


