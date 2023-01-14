
# Important

- First flag given in the config should be spawned by admin and made sure that the gangs place them at the right place, if not placed properly, it has to be removed from json file manually.
- There is no way to remove/destroy the flags in code.
- Make sure to follow this step properly.


# Items

- Add the following items to shared.lua

```lua
	['ballas_flag'] 				 = {['name'] = 'ballas_flag', 			  	  	['label'] = 'Ballas Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'ballas_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Ballas Flag'},

    ['vagos_flag'] 				 = {['name'] = 'vagos_flag', 			  	  	['label'] = 'Vagos Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'vagos_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Vagos Flag'},

    ['gsf_flag'] 				 = {['name'] = 'gsf_flag', 			  	  	['label'] = 'GSF Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'gsf_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'GSF Flag'},

    ['lost_flag'] 				 = {['name'] = 'lost_flag', 			  	  	['label'] = 'Lost MC Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'lost_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Lost MC Flag'},

    ['ballas_first_flag'] 				 = {['name'] = 'ballas_first_flag', 			  	  	['label'] = 'Ballas First Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'ballas_first_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Ballas First Flag'},

    ['vagos_first_flag'] 				 = {['name'] = 'vagos_first_flag', 			  	  	['label'] = 'Vagos First Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'vagos_first_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Vagos First Flag'},

    ['gsf_first_flag'] 				 = {['name'] = 'gsf_first_flag', 			  	  	['label'] = 'GSF First  Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'gsf_first_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'GSF First  Flag'},

    ['lost_first_flag'] 				 = {['name'] = 'lost_first_flag', 			  	  	['label'] = 'Lost MC First Flag', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'lost_first_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Lost MC First Flag'},

    ['shovel'] 				 = {['name'] = 'shovel', 			  	  	['label'] = 'Flag Removal Shovel', 			['weight'] = 500, 		['type'] = 'item', 		['image'] = 'lost_flag.png', 	 ['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Used to destroy/remove flags'},
```

# Features
- Gangs can buy one flag and one flag removal once every tsunami.
- Price of gang flags increase as they keep on buying it. (more flags, more money, multiplier is available in config)
- More flags placed, more money they get from selling drugs. Multiplier and everything is present in config.
- Event to trigger to buy flags/removal is given in cl_buyflags.lua. Trigger that event through qb-target or wherever you want to.
- Lot of configurable values to play with the count of gang members, time required to rob, etc are present in config.lua
- Make sure to read through unencrypted files to edit target options, notification, mail, etc to suit your needs.
- Flags can be placed next to each other and doesnt allow players to place their gang flags all over the place
- Can add as many gangs you want (make sure the props are different so that the targets dont mix up. Check Config to add more gangs and follow it.)
- Option to customize the drugs sold at cornerselling. Can add as many drugs you want.
- Support added for circular progressbar to change font awesome icons
- Reputation factor where more the locals of your gang are robbed, lesser money you make while cornerselling, you need to cornersell more to get build your reputation.
- Everything is persistent i.e it can go through server restarts.
- Blips can be toggled using /toggleblip command (logic can be found in cl_customise.lua)