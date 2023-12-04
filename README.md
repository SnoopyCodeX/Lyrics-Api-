Lyrics API!

### Examples

__Using alternative method (title, artist name, duration)__

```
http://localhost/YourFolder/Ly.php?t=Hope&a=XXXTENTACION&d=1:50&type=alternative
```
__Using default method__

```
http://localhost/YourFolder/Ly.php?q=Here Comes The Sun%20The Beatles&type=default
```
response:

```
[00:15.05]Here comes the sun, doo-doo-doo-doo
[00:18.77]Here comes the sun, and I say
[00:22.07]It's alright
[00:25.08]♪
[00:27.54]Little darlin', it's been a long, cold, lonely winter
```

### How to use
__Lyrics Synced Alternative__

```Php

    include_once("./Ly.php");

    $musix = new MusixLyricsApi\Musix(); 
    echo $musix->getLyricsAlternative("Here Comes The Sun", "The Beatles");

```

__Lyrics Synced Default__

```Php
    include_once("./Ly.php");

    $musix = new MusixLyricsApi\Musix();
    $track_id = $musix->searchTrack("Hope XXXTENTACION");      
    echo $musix->getLyrics($track_id);
```
