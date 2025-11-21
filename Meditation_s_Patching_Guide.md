# How to Patch Roblox clients (Made by meditation/meditext):

## Player (2013-2017E):

You need:
- x32DBG
- RbxSigtools 
- and a proper site.

Go to your ROBLOX Client in x32dbg and then press "Symbols" then select "RobloxPlayerBeta.exe";

Click in "Strings" and will load every string in the player. (has the Az icon)

### DOMAIN REPLACEMENT
Search "roblox.com".

Right click and select dump and replace every roblox.com with your domain with 10 characters.

**(If you have a 14 character domain, then search "robloxlabs.com" and replace it.)**

After you replaced it, Open AppSettings and replace the "BaseURL" to your domain.

### PUBLIC KEY REPLACEMENT

Use RbxSigTools and open the "PublicKeyBlob.txt"

Go to "Strings" and search "Bgiaa"

Open in dump (Select the last one at the menu) and replace it.

For android mobile clients: [android patch guide](https://github.com/TheGuyWhoIsIdiot/meditation-s-Patching-guides/blob/main/android%20patch.md)

## RCCService:

**Do the same steps in the Player btw.**

### Infinite JobId 

**Now you need the HxD for this.**

Search in hex "00 00 00 00 00 c0 82 40" and change to "00 00 f8 1f 5f a0 02 42".

**(This will make the RCC not shut down randomly. ~~Better instead of using SOAP~~)**
Quick note here: if you use this in production, you should **not** use this for a production grade, because this can absolutely glitch out the RCC and cause severe memory leakage problems.

### Camera Fix (2015)

I removed this section because the issue is actually related to the client not loading the provided camera script, and can be fixed with these fflags:
FFlagUsesNewCameraFrustum (False)
DFFlagUseLuaCameraAndControl (False, this will make it use pre-2015M camera)


Aftermath: If you did this correctly, contrags now use it for your revival, idc if this is going to get skidded or not.

