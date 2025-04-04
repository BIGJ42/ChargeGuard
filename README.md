# Chargeguard
This is fork of charge limiter by
macOS app to set battery charge limit for Intel MacBooks

## Description

This app modifies a parameter called `BCLM` (presumably "Battery Charge Level Max") in the SMC which limits the charge of the battery to a set value. It also modifies a parameter called `BFCL` ("Battery Final Charge Level") which controls the MagSafe LED indicator light to display the correct status.

The source code can be viewed by opening `src/Charge Limiter.app` in Apple's Script Editor. It is written in Javascript Application Scripting (or JXA).

The companion `bclm` binary (located under `src/Charge Limiter.app/Contents/Resources`) was copied from [this repository](https://github.com/zackelia/bclm). The source code for `bclm` is also available there.

## Releases

Download the latest version from the releases tab.

## Running

After setting a charge limit, the app will silently run and reapply the desired charge level again if you restart your Mac. If you wish to fully charge the battery again, set the charge limit to "100". This will also remove the charge limit persistency on boot. Afterwards, if you do not need the app anymore you can safely move it to the trash.

If you are running macOS High Sierra (10.13) or older, you may need to install [Swift 5 Runtime Support](https://support.apple.com/kb/dl1998?locale=en_US).

## Updates

This app will automatically check and notify you for any updates when you run it.
