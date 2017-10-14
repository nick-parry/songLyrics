# songLyrics


I was tired of manually googling for songlyrics and reading through them to see what I just heard. It will make a
minor attempt at censoring out a couple swear words with green text for better visibility.

The reason this is just a crusty ol' bash script was to try and not use any 3rd party extras(just curl, sed, awk,
uniq, and other more or less standard tools).

If you find any thing that doesn't work straight out of the box, create an issue or let me know what it is that you found.


## Pre Reqs
In the way of dependencies, I don't think there are any. I think you can just run it. But I reserve
the right to be wrong. I use Ubuntu 14.04 on the daily. I wrote this when I was running Ubnuntu 12.04,
but when I upgraded to 14.04, I don't recall making any changes to this script to make it work. I would love to hear
about someone running this on some other distro/verison of bash. I am running bash version `4.3.11(1)-release`.


## Installation
I have cloned the repo in a goofy GIT directory on my box, and a sym-link in my $PATH. Something like this(~/bin is in my path):
```
nick.parry@nparry-laptop:~$ file bin/songLyrics 
bin/songLyrics: symbolic link to `../GIT/songLyrics/songLyrics' 
```

## Usage
 To display lyrics for a given artist and song title 
 
 `songLyrics <artist> <title>`

 To look up info for the currently playing song in Spotify

`songLyrics spotify`

 To look up info for the currently playing song in Rhythmbox
 
`songLyrics rhythmbox|rbox`

To display the lyrics from a given songlyrics.com url

`songLyrics <songlyrics.com url>`

To display the lyrics from a given azlyrics.com url

`songLyrics <azlyrics.com url>`


## Special cases of goofy-ness 
1) During the general text cleanup, there is a `uniq` at the end of the sed search and replacing.
The purpose of this is to suppress more than one empty line.(E.G. If there are 10 empty lines,
collapse them into one line. This is suprisingly difficult with something like sed and awk so I
punted and used uniq. The side effect is that you might get 20 lines that say `la la la` silently
collapsed into one line. That didn't seem that bad to me. Let me know if you find a way that this
causes an error.
 
 
## Want to make it better?
Hit me up with a pull request of a neatly committed feature branch that your forked from this.
 


