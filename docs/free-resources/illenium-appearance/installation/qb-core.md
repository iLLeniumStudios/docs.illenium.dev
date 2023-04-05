---
title: "qb-core Installation"
---

### Remove Old Clothing Resources

- Delete `qb-clothing` or `fivem-appearance` from your resources folder
- Delete any tattoo shop resources e.g., `qb-tattooshop` from your resources folder

### Install dependencies

- Download the latest `ox_lib.zip` from [here](https://github.com/overextended/ox_lib/releases/latest)
- Open `ox_lib.zip` and copy the `ox_lib` folder to your server's `resources` folder
- Add `ensure ox_lib` right after `ensure qb-core` in your server.cfg 

### Download illenium-appearance

- Go to the latest release: [here](https://github.com/iLLeniumStudios/illenium-appearance/releases/latest)
- Download `illenium-appearance.zip` from the release

### Add it to your server

- Open `illenium-appearance.zip` and copy the `illenium-appearance` folder to your server's `resources` folder
- Add `setr illenium-appearance:locale "en"` in your server.cfg
- Put `ensure illenium-appearance` right after `ensure ox_lib` in your server.cfg. At the end, the ensured resources should look like this
```haproxy
ensure ox_lib
ensure qb-core
ensure illenium-appearance
```
- Delete the table `player_outfits` and `playerskins` table (if you don't want to migrate) from your database
- Apply the following SQL files to your database to have the new tables created:
    - [playerskins](https://github.com/iLLeniumStudios/illenium-appearance/blob/main/sql/playerskins.sql)
    - [player_outfits](https://github.com/iLLeniumStudios/illenium-appearance/blob/main/sql/player_outfits.sql)
    - [player_outfit_codes](https://github.com/iLLeniumStudios/illenium-appearance/blob/main/sql/player_outfit_codes.sql)
- Remove `qb-clothing` from the `dependencies` section of fxmanifest.lua in `qb-houses` and `qb-apartments`
- Restart your server
