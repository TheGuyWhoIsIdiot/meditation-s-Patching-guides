# tutorial how to do it (THIS IS UNDER WORK THIS GUIDE, BECAUSE I'M DOING THAT WHILE I'M TRYING TO COMPILE THE ANDROID CLIENT)
## Requirements:
- Android studio version 1.5.0 to 2.2.3
- bricks game source code
- a brain
- a gud computar
-# I USED CHAT GPT 😭 because i am super dumb doing fixes, but credit ai for 20% of the fix

## Step 1: Brick up the client
You need to download android studio (modern versions doesnt work yuck 🤢) to compile it, also make sure you have your source code.
-# i hate lazy ppl who wasnt able to touch android src
this is weird that step because you need to do uhhh

## Step 2: fix build.grape 🍇
ok this is crucial because it will display a lot of errors;

Copy this line of code on build.grapes and make sure its on ANDROID FILE OR I WILL KILL YOU 😡😡😡😡😡

`buildscript {
    repositories {
        mavenCentral()
        maven { url 'https://maven.fabric.io/public' }
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.2.3' // Depending what version of your android studio.
        classpath 'io.fabric.tools:gradle:1.25.4' // "A compatible version of the Fabric plugin" - chat gpt
    }
}`
If you didnt apply that, well uhhm you will def get a lot of errors relacted to amazondebug, dont tell me why.

After applying that, it should work that crap, but we will have another problem...

## Step 3: add icon 🚀
"No resource found that matches the given name (at 'icon' with value '@drawable/ic_launcher')."
Idk what roblox was thinking of, but its a **terrible idea** not putting your icons in every build.

To fix that is just simple.
just put the god damn icon; that's how.

## Step 4: Under construction 🚧
This guide is not complete, also if you reached so far, congrats 🥳, i think you compiled correctly your android client by doing that. tho it's currently at work in progress and soon more stuffs will be given to how to compile a client!

# CREDIT ME OR I WILL GET YOU 😠
