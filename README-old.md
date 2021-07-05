<img src="https://github.com/GTAmodding/re3/blob/master/logo.png?raw=true" alt="re3 logo" width="200">

[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2FGTAmodding%2Fre3%2Fbadge%3Fref%3Dmaster&style=flat)](https://actions-badge.atrox.dev/GTAmodding/re3/goto?ref=master)
<a href="https://discord.gg/ERYg58ttcE"><img src="https://img.shields.io/badge/discord-join-7289DA.svg?logo=discord&longCache=true&style=flat" /></a>

Inspired by [Lumen](https://lumendatabase.org/topics/1) (*formerly Chilling Effects*) and [Google](https://cloud.google.com/storage/docs/dmca), this repo contains the text of DMCA takedown notices and counter-notices we've received here at GitHub. We publish them as they are received, redacting only private information, as well as URLs reported but that we determined were not actionable under the DMCA.
## Intro

In this repository you'll find the fully reversed source code for GTA III ([master](https://github.com/GTAmodding/re3/tree/master/) branch) and GTA VC ([miami](https://github.com/GTAmodding/re3/tree/miami/) branch).

It has been tested and works on Windows, Linux and FreeBSD, on x86, amd64, arm and arm64.\
Rendering is handled either by original RenderWare (D3D8)
or the reimplementation [librw](https://github.com/aap/librw) (D3D9, OpenGL 2.1 or above, OpenGL ES 2.0 or above).\
Audio is done with MSS (using dlls from original GTA) or OpenAL.

The project has also been ported to the [Nintendo Switch](https://github.com/AGraber/re3-nx/),
[Playstation Vita](https://github.com/Rinnegatamante/re3) and
[Nintendo Wii U](https://github.com/GaryOderNichts/re3-wiiu/).

We cannot build for PS2 or Xbox yet. If you're interested in doing so, get in touch with us.

## Installation

- re3 requires PC game assets to work, so you **must** own [a copy of GTA III](https://store.steampowered.com/app/12100/Grand_Theft_Auto_III/).
- Build re3 or download the latest nightly build:
  - [Windows D3D9 MSS 32bit](https://nightly.link/GTAmodding/re3/workflows/re3_msvc_x86/master/re3_Release_win-x86-librw_d3d9-mss.zip)
  - [Windows D3D9 64bit](https://nightly.link/GTAmodding/re3/workflows/re3_msvc_amd64/master/re3_Release_win-amd64-librw_d3d9-oal.zip)
  - [Windows OpenGL 64bit](https://nightly.link/GTAmodding/re3/workflows/re3_msvc_amd64/master/re3_Release_win-amd64-librw_gl3_glfw-oal.zip)
  - [Linux 64bit](https://nightly.link/GTAmodding/re3/workflows/build-cmake-conan/master/ubuntu-latest-gl3.zip)
  - [MacOS 64bit](https://nightly.link/GTAmodding/re3/workflows/build-cmake-conan/master/macos-latest-gl3.zip)
- Extract the downloaded zip over your GTA 3 directory and run re3. The zip includes the gamefiles and in case of OpenAL the required dlls.

## Screenshots

![re3 2021-02-11 22-57-03-23](https://user-images.githubusercontent.com/1521437/107704085-fbdabd00-6cbc-11eb-8406-8951a80ccb16.png)
![re3 2021-02-11 22-43-44-98](https://user-images.githubusercontent.com/1521437/107703339-cbdeea00-6cbb-11eb-8f0b-07daa105d470.png)
![re3 2021-02-11 22-46-33-76](https://user-images.githubusercontent.com/1521437/107703343-cd101700-6cbb-11eb-9ccd-012cb90524b7.png)
![re3 2021-02-11 22-50-29-54](https://user-images.githubusercontent.com/1521437/107703348-d00b0780-6cbb-11eb-8afd-054249c2b95e.png)

## Improvements

We have implemented a number of changes and improvements to the original game.
They can be configured in `core/config.h`.
Some of them can be toggled at runtime, some cannot.

#### Anatomy of a takedown notice

In the spirit of transparency, we post each takedown notice that we process without making any changes to the text, except for redacting private information and URLs that were not actionable, and adding a few annotations to help you better understand how we processed the notice. Here are the annotations you might see and what they mean.
1. **We gave repository owners a chance to make changes before we processed the notice.** 

When you see this at the top of a notice (starting in March 2021)
>Before disabling any content in relation to this takedown notice, GitHub
>- contacted the owners of some or all of the affected repositories to give them an opportunity to make changes that could have prevented the need to disable the content 
>- provided information on how to [submit a DMCA Counter Notice](https://docs.github.com/en/articles/guide-to-submitting-a-dmca-counter-notice). 

it means that either the notice did not allege that the entire contents of a repository infringe, or the copyright holder identified other changes that could be made to the content to resolve the alleged infringement. As we note in our [DMCA Takedown Policy](https://docs.github.com/en/github/site-policy/dmca-takedown-policy#a-how-does-this-actually-work), in those cases, because GitHub cannot disable access to specific files within a repository, we will contact the user who created the repository and give them approximately 1 business day to delete or modify the content specified in the notice. 

If the repository owner makes the necessary changes, then GitHub will not disable the content. In some cases, that means the repositories are currently available despite being listed in the notice. In other cases, a repository might be unavailable because the repository owner decided to delete it.

Note, none of this is new policy - what's new as of March 2021 is that we are now adding this annotation in any posted notice we process this way. 

2. **We only processed the takedown notice with respect to some of the reported URLs.** 
>[invalid]

or
>[private]

In many cases a notice alleges copyright infringement in multiple repositories or files. When we determine that only some of the repositories or files are infringing, including where reported content was not available at the time we reviewed the notice, we replace the other URLs with `[invalid]`. Before March 2021, we had replaced those URLs with `[private]`, which we continue to use to note redaction of private information.

3. **The notice reported a repository that's being actively forked.** 

As of March 2021, you may see this note where a takedown notice reports an allegedly infringing repository that was being actively forked at the time it was reported
>[Note: Because the parent repository was actively being forked when this DMCA takedown notice was received, and the submitter had identified all known forks at the time they submitted the takedown notice, GitHub processed the takedown notice against the entire fork network of [x] forks.]

As we explain in our [DMCA Takedown Policy](https://docs.github.com/en/github/site-policy/dmca-takedown-policy#b-what-about-forks-or-whats-a-fork), in those rare cases when a notice alleges copyright infringement in a full repository that is actively being forked, we would process a valid claim against all forks in that network at the time we process the notice, if the notice identified all existing forks of that repository as allegedly infringing. We would do this given the likelihood that all newly created forks would contain the same content as those existing at the time the notice was submitted. 

4. **The notice reported a repository with more than 100 forks.**

As of March 2021, if you see this statement in a notice
>Based on the representative number of forks I have reviewed, I believe that all or most of the forks are infringing to the same extent as the parent repository.

it means the reported network that contains the allegedly infringing content was larger than one hundred (100) repositories and thus would have been difficult to review in its entirety. As a result, we disabled the entire network because the submitter reviewed a representative sample of the forks in the network such that they were fairly certain the entirety of the network was infringing and included that sworn statement as part of their takedown notice. In these cases, we note in the takedown notice the total number of forks we disabled at the time of processing.
* Fixed a lot of smaller and bigger bugs
* User files (saves and settings) stored in GTA root directory
* Settings stored in re3.ini file instead of gta3.set
* Debug menu to do and change various things (Ctrl-M to open)
* Debug camera (Ctrl-B to toggle)
* Rotatable camera
* XInput controller support (Windows)
* No loading screens between islands ("map memory usage" in menu)
* Skinned ped support (models from Xbox or Mobile)
* Rendering
  * Widescreen support (properly scaled HUD, Menu and FOV)
  * PS2 MatFX (vehicle reflections)
  * PS2 alpha test (better rendering of transparency)
  * PS2 particles
  * Xbox vehicle rendering
  * Xbox world lightmap rendering (needs Xbox map)
  * Xbox ped rim light
  * Xbox screen rain droplets
  * More customizable colourfilter
* Menu
  * Map
  * More options
  * Controller configuration menu
  * ...
* Can load DFFs and TXDs from other platforms, possibly with a performance penalty
* ...

## To-Do

The following things would be nice to have/do:

* Fix physics for high FPS
* Improve performance on lower end devices, especially the OpenGL layer on the Raspberry Pi (if you have experience with this, please get in touch)
* Compare code with PS2 code (tedious, no good decompiler)
* [PS2 port](https://github.com/GTAmodding/re3/wiki/PS2-port)
* Xbox port (not quite as important)
* reverse remaining unused/debug functions
* compare CodeWarrior build with original binary for more accurate code (very tedious)

## Modding

Asset modifications (models, texture, handling, script, ...) should work the same way as with original GTA for the most part.

Mods that make changes to the code (dll/asi, CLEO, limit adjusters) will *not* work.
Some things these mods do are already implemented in re3 (much of SkyGFX, GInput, SilentPatch, Widescreen fix),
others can easily be achieved (increasing limis, see `config.h`),
others will simply have to be rewritten and integrated into the code directly.
Sorry for the inconvenience.

## Building from Source  

When using premake, you may want to point GTA_III_RE_DIR environment variable to GTA3 root folder if you want the executable to be moved there via post-build script.

Clone the repository with `git clone --recursive https://github.com/GTAmodding/re3.git`. Then `cd re3` into the cloned repository.

<details><summary>Linux Premake</summary>

For Linux using premake, proceed: [Building on Linux](https://github.com/GTAmodding/re3/wiki/Building-on-Linux)

</details>

<details><summary>Linux Conan</summary>

Install python and conan, and then run build.
```
conan export vendor/librw librw/master@
mkdir build
cd build
conan install .. re3/master@ -if build -o re3:audio=openal -o librw:platform=gl3 -o librw:gl3_gfxlib=glfw --build missing -s re3:build_type=RelWithDebInfo -s librw:build_type=RelWithDebInfo
conan build .. -if build -bf build -pf package
```
</details>

<details><summary>FreeBSD</summary>

For FreeBSD using premake, proceed: [Building on FreeBSD](https://github.com/GTAmodding/re3/wiki/Building-on-FreeBSD)

</details>

<details><summary>Windows</summary>

Assuming you have Visual Studio 2015/2017/2019:
- Run one of the `premake-vsXXXX.cmd` variants on root folder.
- Open build/re3.sln with Visual Studio and compile the solution.

Microsoft recently discontinued its downloads of the DX9 SDK. You can download an archived version here: https://archive.org/details/dxsdk_jun10

**If you choose OpenAL on Windows** You must read [Running OpenAL build on Windows](https://github.com/GTAmodding/re3/wiki/Running-OpenAL-build-on-Windows).
</details>

> :information_source: premake has an `--lto` option if you want the project to be compiled with Link Time Optimization.

> :information_source: There are various settings in [config.h](https://github.com/GTAmodding/re3/tree/master/src/core/config.h), you may want to take a look there.

> :information_source: re3 uses completely homebrew RenderWare-replacement rendering engine; [librw](https://github.com/aap/librw/). librw comes as submodule of re3, but you also can use LIBRW enviorenment variable to specify path to your own librw.

If you feel the need, you can also use CodeWarrior 7 to compile re3 using the supplied codewarrior/re3.mcp project - this requires the original RW33 libraries, and the DX8 SDK. The build is unstable compared to the MSVC builds though, and is mostly meant to serve as a reference.

## Contributing
As long as it's not linux/cross-platform skeleton/compatibility layer, all of the code on the repo that's not behind a preprocessor condition(like FIX_BUGS) are **completely** reversed code from original binaries.  

We **don't** accept custom codes, as long as it's not wrapped via preprocessor conditions, or it's linux/cross-platform skeleton/compatibility layer.

We accept only these kinds of PRs;

- A new feature that exists in at least one of the GTAs (if it wasn't in III/VC then it doesn't have to be decompilation)  
- Game, UI or UX bug fixes (if it's a fix to original code, it should be behind FIX_BUGS)
- Platform-specific and/or unused code that's not been reversed yet
- Makes reversed code more understandable/accurate, as in "which code would produce this assembly".
- A new cross-platform skeleton/compatibility layer, or improvements to them
- Translation fixes, for languages original game supported
- Code that increase maintainability  

We have a [Coding Style](https://github.com/GTAmodding/re3/blob/master/CODING_STYLE.md) document that isn't followed or enforced very well.

Do not use features from C++11 or later.


## History

re3 was started sometime in the spring of 2018,
initially as a way to test reversed collision and physics code
inside the game.
This was done by replacing single functions of the game
with their reversed counterparts using a dll.

After a bit of work the project lay dormant for about a year
and was picked up again and pushed to github in May 2019.
At the time I (aap) had reversed around 10k lines of code and estimated
the final game to have around 200-250k.
Others quickly joined the effort (Fire_Head, shfil, erorcun and Nick007J
in time order, and Serge a bit later) and we made very quick progress
throughout the summer of 2019
after which the pace slowed down a bit.

Due to everyone staying home during the start of the Corona pandemic
everybody had a lot of time to work on re3 again and
we finally got a standalone exe in April 2020 (around 180k lines by then).

After the initial excitement and fixing and polishing the code further,
reVC was started in early May 2020 by starting from re3 code,
not by starting from scratch replacing functions with a dll.
After a few months of mostly steady progress we considered reVC
finished in December.

Since then we have started reLCS, which is currently work in progress.


## License

We don't feel like we're in a position to give this code a license.\
The code should only be used for educational, documentation and modding purposes.\
We do not encourage piracy or commercial use.\
Please keep derivate work open source and give proper credit.
