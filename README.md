# Get rid of MeMuPlay advertisement in 2025

[![YT](https://i.ytimg.com/vi/AvWKDF0d-SU/maxresdefault.jpg)](https://www.youtube.com/watch?v=AvWKDF0d-SU)
[https://www.youtube.com/watch?v=AvWKDF0d-SU]()

## Install [Projectivy Launcher](https://github.com/spocky/miproja1/releases)

## Open ADB shell 

```sh
adb -s 127.0.0.1:21503 shell # replace with the address/serial of your Emulator 
pm disable-user --user 0 com.android.internal.display.cutout.emulation.corner
pm disable-user --user 0 com.android.internal.display.cutout.emulation.double
pm uninstall -k --user 0 "$(cmd shortcut get-default-launcher | head -n1 | awk -F{ '{print $2 }' | awk -F/ '{print $1 }')"
#pm uninstall -k --user 0 com.microvirt.launcher2
am start "$(cmd package resolve-activity --brief com.spocky.projengmenu | tail -n 1)"
settings put secure enabled_accessibility_services com.spocky.projengmenu/com.spocky.projengmenu.services.ProjectivyAccessibilityService

# Follow the instructions on the screen, and grant the rights the Launcher needs 

```

## Select "override current launcher" in Projectivy Launcher's option 

## Reboot the emulator, and enjoy gaming/botting without ads

