#CS2 Config
## Commands

```
$config_dir=pwd
$cs2_dir="C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg"

cd $cs2_dir
New-Item -Path startup.cfg -ItemType SymbolicLink -Value "${config_dir}\startup.cfg"
```
## Config content
// [ VOLUME ]
alias default_volume "volume 0.5"
alias boosted_volume "volume 1"

// set "default" volume
default_volume

// [ FPS SETTINGS ]
// set to screen refresh rate
fps_max_ui 84
fps_max_tools 84
fps_max 168

// [ BUY BINDS ]
bind kp_divide "buy tec9; buy fiveseven"
bind kp_multiply "buy p250"
bind kp_minus "buy deagle"
bind kp_plus "buy ssg08"

bind kp_7 "buy ak47; buy m4a1_silencer"
bind kp_8 "buy galilar; buy famas"
bind kp_9 "buy mac10; buy mp9"

bind kp_4 "buy vesthelm"
bind kp_5 "buy vest"
bind kp_6 "buy defuser"

bind kp_1 "buy smokegrenade"
bind kp_2 "buy flashbang"
bind kp_3 "buy molotov; buy incgrenade"
bind kp_del "buy hegrenade"

// [ MOVEMENT BINDS ]
bind MOUSE_X "yaw"
bind MOUSE_Y "pitch"

bind mouse1 "+attack"
bind mouse2 "+attack2"

bind w "+forward"
bind s "+back"
bind a "+left"
bind d "+right"

bind space "+jump"

bind e "+use"
bind r "+reload"

// set volume to "boosted" when walking
alias +volwalk "boosted_volume; +sprint"
alias -volwalk "default_volume; -sprint"
bind alt +volwalk

// set volume to "boosted" when crouching
alias +volcrouch "boosted_volume; +duck"
alias -volcrouch "default_volume; -duck"
bind c +volcrouch

// [ COMMUNICATION BINDS ]
bind v "+voicerecord"
// all chat
bind j "messagemode"
// team chat
bind k "messagemode2"

bind mouse3 "player_ping"

// [ OTHER BINDS ]
bind tab "+showscores"
bind m "teammenu"

// [ EQUIPMENT BINDS ]
// primary
bind "1" "slot1"
// pistol
bind "2" "slot2"
// knife
bind "3" "slot3"
// cycle grenades
bind "4" "slot4"
// bomb
bind "5" "slot5"

// he grenade
bind g "slot6"
// flashbang
bind f "slot7"
// smoke grenade
bind mouse5 "slot8"
// decoy grenade
bind z "slot9"
// molotov / incendiary grenade
bind t "slot10"

// healthshot
bind x "slot12"

bind b "buymenu"

// drop
bind q "drop"

// drop bomb
alias "+bomb" "use weapon_knife; slot5"
alias "-bomb" "drop"
bind z "+bomb"

// [ TRAINING ]
bind p "sv_cheats 1; sv_rethrow_last_grenade"
bind l "sv_cheats 1; noclip"

// [ SUCCESS ]
echo "'startup.cfg' loaded"
