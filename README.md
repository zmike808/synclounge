# Plex Together

Plex Together is a tool to sync Plex content across multiple players in multiple locations.

This early alpha release does not include a compiled binary. If you are unfamiliar with debugging, NodeJS and port forwarding, this release is not for you. But don't worry! In the near future we'll be releasing a more user friendly update which includes public PlexTogether servers for everyone to use if they want.

## How it works
Plex Together aims to keep multiple viewing sessions in sync regardless of whether the clients are in the same room or across the globe. To do this Plex Together utilizes a middle-man server to communicate between each of Plex Together clients. Users choose their Plex client, decide on a Plex Together Server and Room name and join up. Friends can then also do the same. Whoever joins first will become the host. 

The host has complete control over a room. Commands they send to their client will be sent through to other people in the room (Play, Pause, Seek etc). If the host starts playing something different, Plex Together will search all of your available Plex Media Servers for an equiavalent copy, even if it is not from the same Plex Media Server as the Host.  

## Features
* Syncing between Plex Clients over the Internet
* Automatic searching of content across all your Plex Media Servers
* Searching from Shared Plex Media Servers
* Metadata fetching from Plex Media Server
* Password locked rooms
* Movies and TV Shows
* Restrict auto play to a specific Plex Media Server

## Screenshots

![Playback](http://plextogether.com/img/6-0playback.png)

For more screenshots, head to the website at http://plextogether.com
----
## Supported Plex Clients
Theoretically, all Plex Clients that implement the Plex Client Protocol will work. As some clients have this implemented slightly differently, compability with Plex Together may vary. If you have access to one of the untested clients please let us know how it goes.
### Tested and working
* Plex Home Theatre
* OpenPHT
* Rasplex
* Plex Media Player 
* Apple TV
* iOS (iPhone & iPad)
* Rasplex
* Plex Web Player (Chrome)
### Untested 
#### Computer
* Windows 10 App 
* Kodi
#### Streaming Devices
* Amazon Fire TV  
* Roku
* Android TV
* Chromecast
* TiVo
* Sonos
#### TVs and Consoles		
* Xbox One
* Xbox 360
* PS3
* PS4
* Nvidia Shield
* Smart TV
#### Mobile
* Android
* Windows Phone

----

## Getting Started

You need:

* Node v6+
* A stable Internet connection
* With node installed either you or your friend will need to run the PT Server. You can run the PT Server from the same machine, but depending on your network setup you may need to enable port forwarding on your router to let others connect. 

## Running PT Client on macOS & Windows

You will need to run Plex Together from the command line:
* Clone this repo
* Navigate to Plex Together directory
* Install dependencies with npm:
  * ``npm install``
* Run using npm
	* ``npm start``

## Running PT Server on macOS, Ubuntu & Windows
* Clone this repo
* cd to the server directory
* Run the server
	* ``node index.js``
* By default, the server will listen on 0.0.0.0:8088. Feel free to change this if that port is in use.
----
## Using Plex Together
Once you've run the app please follow the below steps:

1. Log in with your plex.tv credentials
2. Select your player (make sure the player is open on your device of choice)
3. Click 'Join Room'
	* Enter IP:PORT/URL of PT Server
	* Enter room name + password (if applicable)
	* note - if you see a STAR next to your name you are the host.

Once the above is done you're all set! Depending on whether you're the host or a participant will determine your next steps:

**HOST** - Once all your friends have begun you may start your media in your Plex Player.

**PARTICIPANT** - Wait for the host of the room to start playing media. If the media does not start playing automatically you may manually play the media on your client.

----
## License

Plex Together is licensed under MIT License. See the ``LICENSE.txt`` file.
Plex Together is in no way affiliated with Plex Inc.
