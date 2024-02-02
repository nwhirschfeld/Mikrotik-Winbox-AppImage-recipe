# Mikrotik-Winbox-AppImage-recipe
recipe to build an appimage with winbox and wine

## building the AppImage

You can use the following command in the cloned repo to build the appimage using podman:

``` console
$ podman run -v "./:/winbox" -it --security-opt label=disable appimagecrafters/appimage-builder:latest '/bin/bash' -c "cd /winbox && appimage-builder --recipe AppImageBuilder.yml --skip-tests"
```

## Special Thanks to Alexis Lopez Zubieta

A huge thank you to Alexis Lopez Zubieta for his incredible [blog post](https://azubieta.net/p/packing-portable-windows-apps-for-linux/), this recipe is based on. 
