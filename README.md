# preinstalled-app-remover

> **Clearing the uninstallable junk that eats the home screen on an old low-spec handset**

- - -

## Contents

1. [What this is](#what-this-is)
1. [Running it](#running-it)
1. [Known limits](#known-limits)
1. [Helping out](#helping-out)
1. [Where it came from](#where-it-came-from)
- - -

## What this is

Every handset ships with software nobody asked for and nobody can remove from the settings screen: extra browsers, storefronts, payment apps, cloud clients, mail clients, accessibility helpers. Those packages drain storage and never go away through normal means. This little desktop utility removes them, using nothing more than an unlocked debug bridge over a plain data cable.

![Application Interface](./res/app.png)

The window is built with `tkinter`. An `adb` binary talks to the handset shell over USB and reaches the package manager; a small asset tool is pushed into a scratch folder on the phone, reads the installed package list, and reports back. Every package shows up with a checkbox, so you can search and tick what you want gone. Pressing `Clean` strips them immediately. Anything removed can be brought back by side-loading it again or by factory resetting the phone. When the window closes, the pushed tool is deleted from the device automatically.

- - -

## Running it

1. **Unpack** the archive from the releases page.

1. ***Enable developer options and USB debugging*** on the handset.

1. ***Plug it into the computer*** in file-transfer mode and accept the debugging prompt on the screen.

1. **Start the executable** and wait for the package scan to finish.

1. The rest is self-explanatory.

- - -

## Known limits

1. Devices locked down by Samsung's enterprise security layer refuse to cooperate.

1. If the debugging prompt is accepted late (step 3 above), restart the utility.

1. Scrolling behaves only when the pointer sits over the scrollbar.

- - -

## Helping out

Search support, wireless transfer and restore-from-backup are on the wish list. Pull requests toward any of those are appreciated.

----------------------------------------

## Where it came from

**Thanks for trying it.** The whole thing exists because of one very slow phone. I did not get a handset of my own until after secondary school; before that I dug an abandoned one out of storage and tried to make it usable. The stock apps made it crawl, no tool existed to clear them, so this got written instead.

> ❤️‍🔥 built out of frustration ❤️‍🔥