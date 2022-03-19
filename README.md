# Native Minecraft on M1 Apple Silicon (OptiFine)
> Run Minecraft natively on Apple Silicon, using the default launcher and optifine.

This is based off of:
https://gist.github.com/ezfe/8bc43a65e16b79c955f81b4d7fa4ae6a#file-1-18-1-arm64-json

If you would like to skip the Optifine portion, you can just download it from here following these steps.
  1. Download the correct version you wish to install. You can either download the entire repo, or I may have a RELEASE where you can download a zip.
  2. There will be 1 folder, `<version/optifine>-arm64`. Drag this folder into `~/Library/Application Support/minecraft/versions`.
  3. Ensure that you have the `<version>-arm64` folder already. For example, if you are installing `1.18.2 Optifine`, then follow the steps <a href="https://gist.github.com/ezfe/8bc43a65e16b79c955f81b4d7fa4ae6a#file-1-18-1-arm64-json">here</a>, making sure you name everything `1.18.2-arm64`.
  4. Open your Minecraft launcher and create a new installation. Point the install folder to the `<version/optifine>-arm64` folder. Point the Java installation to where you installed your ARM based java.
  5. Save, and run!

This assumes that you already have a version of ARM based Java installed.

## instructions
  1. Run `<version>` in the official Minecraft launcher, then quit the game & launcher. (skip this step if you've already done so.)
  2. Download OptiFine: <a href="https://optifine.net/downloads">here<a>.
  3. Install OptiFine. Locate where you've downloaded OptiFine and install it by right clicking it, then open. Then hit install. Close when complete.
  3. Open finder and navigate to `~/Library/Application Support/minecraft/versions` (cmd + g)
  4. Rename the original `<version>` folder. For this example, we are doing `1.18.2`. Rename that folder to `1.18.2-arm64`.
  5. Rename the OptiFine `<version/optifine>` folder. For this example, we are doing `1.18.2-OptiFine_HD_U_H6`. Rename that folder to `1.18.2-OptiFine_HD_U_H6-arm64`.
  6. Open the original `<version>` folder. Delete the `<version>.json` file. In this example, we are deleting `1.18.2.json`.
  7. Rename the `<version>.jar` file to `<version>-arm64.jar`. In our example, we will rename `1.18.2.jar` to `1.18.2-arm64.jar.`
  8. Download the modified `<version>-arm64.json` file. I have included some in this repo. Drag that into the same folder from where you deleted `<version>.json`.
  9. Exit the `<version>-arm64` folder. Open the `<version>-optifine-arm64` folder.
  10. Rename both `<version/optifine>.jar` and `<version/optifine>.json` by appending `-arm64` to the end of both.
  11. Open & edit `<version/optifine>-arm64.json`. Rename the "id" by appending `-arm64` to the end.
  12. Edit the line that starts with `inheritsFrom:` to include `-arm64`, so our example would be `1.18.2-arm64`.
  13. Open your Minecraft launcher and create a new installation. Point the install folder to the `<version/optifine>-arm64` folder. Point the Java installation to where you installed your ARM based java.
  14. Save, and run!

## Credits
https://gist.github.com/ezfe
