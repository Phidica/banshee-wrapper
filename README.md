# banshee-wrapper
An extensive Bash script which interfaces with Banshee via the default command line arguments to provide various services

Current features:
* On-demand popup of now-playing information, similar in format to that provided by the Notification Area Icon community extension
* Absolute *and relative* ranking changes to current track

## Screenshots
On GNOME 3.16 (Dark Theme) the notifications provided by banshee-wrapper will look something like:

![screenshot of notification](http://i.imgur.com/xSDj2uB.png)

Figure 1: Display default

![screenshot of notification on hover](http://i.imgur.com/PrxOukO.png)

Figure 2: Display during mouse hover

## Requirements
The script requires the following packages and libraries:
* notify-send

## Installation
Clone the repository with

    $ git clone https://github.com/Rhotias/banshee-wrapper.git

Copy the *banshee-wrapper* file to your directory of choice. *~/.local/bin/* is a good one, if that's on your $PATH. Make the script executable with

    $ chmod +x banshee-wrapper

## Execution
The program accepts the following flags and arguments:

* **-n** : Display a *notify-send* notification with information on the currently-playing track rating, number, title, artist, and album

    The album art shown in this notification is sourced from the Banshee media art cache

* **-r [+|-]x** : Set the current track rating to *x*, or increase/decrease it by *x* (note: Banshee ratings range from 0 to 5)
