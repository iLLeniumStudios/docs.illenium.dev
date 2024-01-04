---
title: "ESX Installation"
---

### Folowing features are not yet supported in ESX
- Boss Managed Outfits (Config.BossManagedOutfits)

- Radial Menu (Config.UseRadialMenu)

### Remove Old clothing resources
- Delete the following from your resources folders:

	- esx_skin

	- skinchanger

	- fivem-appearance

	- esx_barbershop

	- esx_clotheshop

- Also delete any tattoo shop resources e.g., `esx_tattooshop` from your resources folder

### Install dependencies
- Download the latest `ox_lib.zip` from [here](https://github.com/overextended/ox_lib/releases/latest)

- Open `ox_lib.zip` and copy the `ox_lib` folder to your server's `resources` folder

- Add `ensure ox_lib` right after `ensure es_extended` in your server.cfg

### Download illenium-appearance
- Go to the latest release: [here](https://github.com/iLLeniumStudios/illenium-appearance/releases/latest)
- 
- Download `illenium-appearance.zip` from the release

### Add it to your server
- Open `illenium-appearance.zip` and copy the `illenium-appearance` folder to your server's `resources` folder

- Add `setr illenium-appearance:locale "en"` in your server.cfg

- Put `ensure illenium-appearance` right after `ensure ox_lib` in your server.cfg. At the end, the ensured resources should look like this
```lua
ensure  ox_lib
ensure  es_extended
ensure  illenium-appearance
```
- Delete the table `player_outfits` and `playerskins` table (if you don't want to migrate) from your database

- Apply the following SQL files to your database to have the new tables created:

	- [player_outfits](https://github.com/iLLeniumStudios/illenium-appearance/blob/main/sql/player_outfits.sql)
  - [player_outfit_codes](https://github.com/iLLeniumStudios/illenium-appearance/blob/main/sql/player_outfit_codes.sql)

- Do 1 of the following:

	- Search for `esx_skin` and `skinchanger` in all fxmanifest.lua files of your resources and remove all those lines

	- OR

	- Add `provides { "esx_skin", "skinchanger" }` at the end of illenium-appearance/fxmanifest.lua file and save

- Restart your server
