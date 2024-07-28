# How to Patch Roblox clients (Made by meditation):

## Player (2015 - 2016):

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

## RCCService:

(modified after publish: Most of the steps here are avaliable, but other wasnt mentioned.)

**Do the same steps in the Player btw.**

### Infinite JobId 

**Now you need the HxD for this.**

Search in hex "00 00 00 00 00 c0 82 40" and change to "00 00 f8 1f 5f a0 02 42".

**(This will make the RCC not shutdowning randomly. Better instead of using SOAP)**

### Camera Fix (2015)

Some cases, we arent able to use the camera normally, but use this script in gameserver.txt:

```lua
game:GetService('Players').PlayerAdded:connect(function(player) -- Thanks jetray!

player.CharacterAdded:connect(function(char)

local a = game:GetObjects("rbxasset://fonts/characterCameraScript.rbxmx")[1]:Clone()

a.Parent = char

local test = game:GetObjects("rbxasset://fonts/characterControlScript.rbxmx")[1]:Clone()

test.Parent = char

end)

end)
```

Aftermath: If you did this correctly, contrags now use it for your revival, idc if this is going to get skidded or not.
