?> Here is a list of the most Frequently Asked Questions about LÖVE Potion.

### Can I run my LÖVE game on this?

Running your game without any changes is possible, but it's recommended to currently use LÖVE Potion to make games from the ground up.<br>
Take a look at [compatibility](compatibility) and the API reference on the sidebar to see what may need changing.

### Can I run my LÖVE Potion application through emulation?

No, emulation is generally unreliable. It is strongly recommended to use _real_ hardware if you want to test it on-device. Alternatively you can use [nëst](https://github.com/lovebrew/nest) in order to pseudo-test your games.

### Do I need to install all the devkitPro tools to build my game?

No. All you need is the [bundler website](/bundler/index.md). It will automatically convert your assets to the right format and package the game for you.

### Can I help?

Yes, see [Building](building) for more details.

### LÖVE Potion is missing feature 'x' from LÖVE, and I need it!

Well that's great to hear! Please open an issue so that I can keep track of your request. I'll gladly implement what you've asked for, as long as it's feasible.

### Can I use shaders?

No. The 3DS doesn't support the OpenGL Shader Language, which is what LÖVE uses. Shader programs for PICA200 (the 3DS GPU) need to be written in [picasso](https://github.com/devkitPro/picasso) shader language and pre-compiled.

The Switch and Wii U can use GLSL, but there are differences in implementation and they still need to be pre-compiled, so shaders from your LÖVE game wouldn't *just run*. 

In general, custom shader support is a complex and difficult to implement feature.

### I just got a Lua error! The app crashed! What do I do?

!> Please be advised: we do not support the use of custom firmwares other than Atmosphère.

If it's a programming error, feel free to join the LÖVE Potion Discord community and ask for help!<br>
Should you encounter a different error, such as an arm11 (3DS) or fatal (Switch) exception, please attach the relevant files into a GitHub issue.<br>

arm11 dumps:
- sdmc:/luma/dumps/arm11

fatal exceptions:
- sdmc:/atmosphere/crash_reports

### Neat! I'm gonna send my game to Nintendo and get cartridge of my game and I'll-

Stop right there, this is for Homebrew only. This is not for releasing a real console title. I dunno, contact Nintendo if that's what you want.

### Can this run Mari0?!

You know, if I had a nickel for every time someone asked that since LÖVE Potion first existed, I'd be pretty darn rich. Now for the actual answer: no. Not yet.

### Why did it take so long for game debugging?

I know this is probably not even a frequent question yet, but it will be. Simply put, all this time LÖVE Potion didn't have any proper means to debug other than the "dev build" logger. This output to a file on the SD card, which it's not entirely about the *speed* impact, it's more of the actual SD card's lifespan being affected with a ton of file writes, especially if it's in something like `love.update`.
