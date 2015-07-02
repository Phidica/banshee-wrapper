# banshee-wrapper
A hideous and wholly terrifying Bash script which interfaces with Banshee to provide various services

Current features:
* On-demand popup of now-playing information, similar in format to that provided by the Notification Area Icon community extension
* Absolute *and relative* ranking changes to current track

## Requirements
The script requires the following packages and libraries (most of which come stock):
* python
  * gib
  * sys
* ffmpeg
* notify-send

## Installation
Clone the repository with

    $ git clone https://github.com/Rhotias/banshee-wrapper.git

Copy the *banshee-wrapper* file to your directory of choice. *~/.local/bin/* is a good one, if that's on your $PATH. Make the script executable with

    $ chmod +x banshee-wrapper

## Execution
The program accepts the following flags and arguments:

* **-n** : Display a *notify-send* notification with information on the currently-playing track rating, number, title, artist, and album

    The album art shown in this notification is extracted from the audio file, so may differ from that used by Banshee

* **-r [+|-]x** : Set the current track rating to *x*, or increase/decrease it by *x* (note: Banshee ratings range from 0 to 5)
