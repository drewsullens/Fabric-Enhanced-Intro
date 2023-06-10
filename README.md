# Fabric Enhanced Intro Mod

> A Mod that redesigns the opening and title screen of the game. - Drew Sullens

## 6 June 2023: The Beginning

This is my first time working with Fabric, so note that the code used here will likely be very primitive.  
I want to give an overview of what the mod is/does, and what inspired it:

### Inspiration

This Mod will redefine how Minecraft: Java Edition opens on startup. In Vanilla Minecraft, when booting the game, you are greeted with a bright red screen with the [Mojang Studios logo](https://www.videogameschronicle.com/files/2020/05/Mojang-new-logo.jpg), as well as a loading bar. Once the game finished loading, the loading bar and the logo fade, as well as the red screen, and you are brought to the title screen of Minecraft, with a spinning panoramic image in the background. 

While this is a nice and simple way to start the game, myself and other people on reddit have noticed that Mojang has already created visuals that would serve as a much better opening to Minecraft today. To start, Mojang has already created a clean and smooth intro for their new logo, which was shown off on this [video](https://youtu.be/YosWmbHAr2g?t=67) (timestamp included in link). This alone would be a nice touch, and I don't quite understand why it hasn't been implemented, at least in Bedrock Edition, considering this very intro is already used in Minecraft Dungeons. However, beyond this, they have another great cinematic that they use as an outro for their YouTube channel, which you can see [here](https://youtu.be/sxWa7LTRvbo?t=378) in one of their latest videos.

What if you were to combine these two cinematics together? The Mojang Studios intro fades in from black on startup, and once the loading bar fades, it transitions into their outro via chroma keying, and transitions to an animated gif of the cave scenery with the title UI displayed on top. There have actually already been concepts of this on YouTube, one of which is by TextureOverload which you can see [here](https://youtu.be/Yczs1H9BZm8). As seen in the description, he mentions he was heavily inspired by [u/Moe_Mux_Hagi](https://www.reddit.com/user/Moe-Mux-Hagi/) over on Reddit, so be sure to check him out as well.

### Planning the Mod

So, after seeing many concepts online, I have decided to try to inbed this seamlessly into minecraft through the use of a Fabric Mod. I am hoping to cause minimal lag upon startup, so it can have an "official" feel in game. Here is a brief overview of how I plan the game to open up:

* The client window opens to a black screen, as many games do, instead of the vanilla bright red screen you are immediately shown upon booting the game.
* Once the correct configurations have been applied to the window (resolution, fullscreen, etc), the Mojang Studios animated intro will fade in from black. You can view the intro that will be used [here](https://drive.google.com/file/d/102v7nG26WKWu1LfBTDrtDcdSn_Hrot7Z/view?usp=drive_link) (MUST DOWNLOAD FOR FULL QUALITY - 2160p120), it has been enhanced using AI software for Frame Interpolation and Upscaling; Not the greatest quality, so I may refine it later.
* Once the Mojang Studios animation finishes, it will be replaced by a still shot of the ending frame, which will be unnoticeable.
* From there the game will load with the standard loading bar that appears, and the loading bar will fade when complete.
* The image will then transition to a video which begins with that very same frame with the Mojang Studios logo. The logo will then fade, leaving only the bright red background, as the video zooms out to the cave outro sequence via chroma keying.
* The "Minecraft" logo will be kept from the outro, as it includes a cool animation of the logo falling onto the screen.
* The Main Title UI will fade in on top of this, with the cave background being a (hopefully) seamless gif, so that the lava, lightning flashes, torches, etc. will all still appear to move.
* I also plan to try to remove the text from the bottom of the outro, including the Xbox and Mojang logos, and the "minecraft.net" text. We'll see how that goes.

* **EDIT:** Thanks to [this](https://youtu.be/SYlJOfDjRQM?t=16) concept, it has inspired me to possibly extend this mod further, specifically the part where the camera zooms back out of the cave when clicking singleplayer. The concept of this movement when clicking singleplayer or creating a world or something sounds dope. This will definitely be a later addition, as I will focus on the main intro first, but I will update with any info on this.

### Preparing the Mod

I want to have all assets I need for this mod before I write it, even if it goes south. I already have the Mojang Studios intro, so I can check that off the list. However, I still need a nice chroma edit of the outro from the Minecraft YouTube channel. Unfortunately, the ones created by the community that I have found are either capped at 720p30, or they have already overlayed it with the title screen UI (Singleplayer and Multiplayer buttons, etc). So, I have a few options:

1. Use one of the community made chroma edits of the Minecraft YouTube outro, and consider enhancing it with AI from 720p30 to something more suitable for a game, such as 1080p60, or even 2160p120 if I really want to push it.
2. Use one of the outro clips from the official Minecraft YouTube channel, because their outros are in 1080p, and edit the video frame-by-frame to create my own chroma screen.

Definitely going with 2. Even though I upscaled the Mojang Studios intro, that was simpler considering it was a very simple animation. However, AI upscaling a full minecraft animation seems unlikely to turn out well, however I can still see how it goes. The current plan is to create my own frame-by-frame chroma screen over the 1080p outro clip I will take from one of their YouTube videos. Then I will use AI Frame Interpolation to upscale it from 30fps to at least 60fps for a smoother and more official feel. Frame Interpolation is much more reliable on giving good results than upscaling resolution, so 1080p might just have to stay, but like I said, I will definitely still run some tests, so we'll see.
