=============================================================================
webMedia plugin for Showtime by andreus sebes (andreus.sebes@gmail.com)
=============================================================================

webMedia plugin for Showtime is a free internet source media reader. 
Can read RSS feeds, Imagecast, Podcast, Videocast, Live TV and Live Radio
(rtmp).

I build this plugin for my own use because i wanted more than current
Showtime plugins can give. 
The purpose of this plugin is to have the possibility to read free media
sources avaivable in the Internet.

I thanks Andreas �man for this wonderfull application that is Showtime and
for all the plugin documentation.
I also thanks facanferff and NP for their excelent plugins.

=============================================================================
Release notes
=============================================================================
1.0: Initial version
- Read RSS feeds (RSS, Imagecast, Podcast and Videocast)
- Read Live TV and Live Radio (rtmp)
- Settings for choose if want to aggregate sources
  - By publisher
  - By theme
  - By country (242 countries by default)  
  - By type (6 types by default)
- Read up to four XML data filesfrom HTTP or SMB
- Just need one XML. Just need one URL. No need for a HTTP folder.
- You can choose parental control level (1 to 9) for each source
- You can choose if each source is your favorite
- Extremely flexible, for each source, you can have a simple xml with title
  and link or a more complex xml with title, link, thumbnail, themes,
  publisher, country, type, parental control and if is your favorite 
- Some debug settings


=============================================================================
Licence notes
=============================================================================

Copyright (C) 2011 andreus sebes

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <http://www.gnu.org/licenses/>.

webMedia plugin uses images that are licensed under Creative Commons and some
fetched from the internet. All rights go to the authors.


=============================================================================
Installing
=============================================================================

webMedia, in the future, will be available directly from Showtime plugin
repository.

Meanwhile if you want to install it on your PS3 you have 2 options:
1. Copy the webmedia.zip file to a USB pen drive, open Showtime, go to the
   USB pen drive icon and run webmedia.zip file
2. Copy the webmedia.zip file to using a file or FTP manager:
  Showtime plugin path:
  /dev_hdd0/game/HTSS00003/USRDIR/settings/installedplugins/

  Showtime (Multiman version) plugin path:
  /dev_hdd0/game/BLES80608/USRDIR/st_settings/installedplugins/

=============================================================================
Configuring
=============================================================================

======= LOCALIZATION OF SOURCES XML FILE =======

webMedia reads the sources XML file for adding the media sources. 

By default, and only for example purposes, the path of this file is inside
the zip of the plugin localizated in Showtime directory (see "Installing").

You can unzip the plugin, change the "sources.xml" file and, when your done,
zip the plugin again and put it in showtime.
Please note that this only works in unoffical Showtime versions.
(see readFile in  https://github.com/andoma/showtime/blob/master/docs/plugins.md)

You can also change the localization of this file file by putting HTTP or SMB
paths in the plugin settings.

Examples:
- SMB: smb://192.168.1.10/webmedia/sources.xml
- HTTP: http://192.168.1.10/webmedia/sources.xml
- HTTP: http://pastehtml.com/view/bfsgjamdn.html
- HTTP: http://pastebin.com/raw.php?i=WDVC940d

======= Creating sources XML file =======

Just use the "webmedia-xml-maker.html" file localizated inside the zip of
the plugin.

======= Editing "sources.xml" file =======

Just use the "webmedia-xml-maker.html" file localizated inside the zip of
the plugin for creating a news xml file and then add the new <item> tags
to your old xml file.

======= Live TV and Live Radio RTMPs =======

webMedia, like watchTV plugin (by facanferff), can read rtmp links for
Live TV and Live Radio.
If you want to see more about rtmp links read the excellent tutorial
made by facanferff.
http://psx-scene.com/forums/content/tutorial-get-rtmp-links-tv-streams-others-1288/

======= Other =======

You can use "[WEBMEDIA]" for indicating a local path inside the plugin file
There is a folder "resources" inside the plugin zip file which contains a
subfolder for each group. You can use it.


=============================================================================
Known issues/Questions/FAQ (with Showtime v3.3.328)
=============================================================================

PROBLEM
-------
In PS3, i want to change the localization of the xml file but
showtime doesn't let me enter text
The problem is that Showtime doesn't have a virtual keyboard.
This is a Showtime problem. There is several issues registed.
- https://www.lonelycoder.com/redmine/issues/2
- https://www.lonelycoder.com/redmine/issues/680
- https://www.lonelycoder.com/redmine/issues/687
Workaround: You have 2 options:
1. Connect a USB keyboard to your PS3, then, in showtime, go to webMedia
plugin settings and manualy add your HTTP/SMB URL
2. Use a FTP filemanger and manualy change the configuration file
of the plugin. This file is in:
  Showtime:
  /dev_hdd0/game/HTSS00003/USRDIR/settings/settings/plugins/webmedia
  Showtime (Multiman version):
  /dev_hdd0/game/BLES80608/USRDIR/st_settings/settings/plugins/webmedia
Just add/change the line
	"xmllocalization1": "xxxxxxxxxxx",

PROBLEM
-------
It takes very time to show the sources.
If you enable probe timeout, webMedia probes the sources before displaying it,
there is a setting for configuring the probe timeout. But this is not having
any effect.
This is a Showtime problem. There is an issue registed.
- Timeout not working https://www.lonelycoder.com/redmine/issues/778

PROBLEM
-------
I accepted the ToS, but when i restart Showtime tit appear again
The problem is that Showtime can't save to disk realtime setting change.
This is a Showtime problem. There is an issue registed.
- Save a setting in real time https://www.lonelycoder.com/redmine/issues/780
Workaround: You can force it in the plugin settings.

PROBLEM
-------
I want to use an ATOM feed that webMedia does not read.
webMedia doesn't read Atom feeds
Workaround: Use a website to convert it in real time
Ex:
- http://devtacular.com/utilities/atomtorss/
- http://atom2rss.appspot.com/

PROBLEM
-------
I want to open the RSS feed item link in the browser
Showtime doesn't support this.


