for playing workshop maps:

you must create a file "webapi_authkey.txt" in csgo folder and add there on first line your web api key - generated here https://steamcommunity.com/dev/apikey
restart server
then you can put in console "host_workshop_map 122521875" where 122521875 is id of a map. You can get the id from url https://steamcommunity.com/sharedfiles/filedetails/?id=122521875
after that command the map should start download - there should be some output in console, if not something is wrong. If there is no output try "host_workshop_collection 125499590" - in my case there was an error with "web api" otherwise it failed silently


for download awp_india:
host_workshop_map 125610094

aim_map:
host_workshop_map 122443683

fy_pool_day:
host_workshop_map 122521875


without downloading these maps "aliases.cfg" for these maps won't work!!!!

What is:
configs in /maps/cfg
-> needed for "custom" game mode. In our case the knives round.

file "subscribed_file_ids.txt"
- ids for workshop maps. After restart the server should download latest versions of these files. Didn't work as expected in my case (downloaded just one). Use "host_workshop_map" for manual download.

file "autoexec.cfg" 
- automatically executed at the start. Manually you can do "exec autoexec"

files "gamemode_*_server.cfg"
- files with "_server " overwrites base configs
- for changing gamemodes "gamemodes_server.txt" must be created in csgo folder
- it is recommended to create these "_server" configs as base configs could be rewritten by any csgo update
- more info about game modes: https://developer.valvesoftware.com/wiki/CS:GO_Game_Mode_Commands
- more info about gamemodes_server: https://developer.valvesoftware.com/wiki/Counter-Strike:_Global_Offensive_Dedicated_Servers

console commands:
- check here: https://totalcsgo.com/commands


How to use (when connected as player on server):
rcon_password "password for rcon"
rcon "some command or alias"

e.g.
rcon_password absa
rcon compD          // start competetive mode on de_dust2


