songLyrics
==========

Get the lyrics for a song(possibly the currently playing song in Spotify) in bash.

The main point of this is to not use any 3rd party anything. This is straight curl,
dbus-send, awk, sed, grep, etc. If you find any thing that doesn't work straight out of
the box, create an issue or let me know somehow. I will fix it at my earliest convenience.

# Here is the general flow for this script:
#### Get the song info(Artist and Title)

    - This can be done automatically via dbus-send commands if you are using Rhythmbox or Spotify
    - This can be passed in manually as the first and second arguments
    - This can be avoided if you have a direct url(One of the supported sites obviously)

#### Google the lyrics for a given artist and title
    - It search through the supported sites(one at a time) to get a url from a supported site

#### Scrape the lyrics out of a known page
    - For now, only songlyrics.com and azlyrics.com are supported. Add more if you would like to.




