# csgo-artixlinux
instructions to get working cs go on artix linux


1. run it in linux runtime
2. launch options: gamemoderun LANG=C vblank_mode=0 LD_PRELOAD="" %command% -novid -nojoy -full -vulkan
3. 
````
sudo pacman -S --needed gperftools
game=~/".local/share/Steam/steamapps/common/Counter-Strike Global Offensive"
gamelibdir="$game/bin/linux64"
cp -n "$gamelibdir"/libtcmalloc_minimal.so.0{,.orig}
/bin/cp `whereis libtcmalloc_minimal_debug.so.4|head -n 1|sed -E 's:^.+\s+::'` "$gamelibdir"/libtcmalloc_minimal.so.0
unset game gamelibdir
````
