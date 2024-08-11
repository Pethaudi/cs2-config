$config_dir=pwd
$cs2_dir="C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg"

cd $cs2_dir
New-Item -Path startup.cfg -ItemType SymbolicLink -Value "${config_dir}\startup.cfg"
