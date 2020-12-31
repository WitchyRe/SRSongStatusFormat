# SRSongStatusFormat
Code to support stylizing the Song Status Output file to a standalone HTML page for use in overlays.

## Directions
1. Copy files (songstatus & songstatus.html) directly to your Synth Riders install location:
    Typically: C:\Program Files (x86)\Steam\steamapps\common\SynthRiders
    
That's it.

_If you are changing the page styling and you would like to test your work without loading the game to play just copy the SongStatusOutput.png and SongStatusOutput.txt to the same directory. 

## How it Works

The songstaus file is a template used by Synth Riders to output active song data to a text file (SongStatusOutput.txt). By formatting this file to a variable array that can be consumed by some javascript, we can import it into a local webpage that can formatted and be used as source object in OBS. 

The local webpage is set to reload itself every 10s. This can be modified to your liking. This is done to refresh any changes in the song data as the files update while Synth Riders is being played. 

The output format currently used is a table but this can be modified as well to your liking. This format was used as it was simple to manage and place on the page by utilizing the CSS positioning of absolutes. The positioning variables on the table determine its location. Currently it is set 50 pixels from the bottom left margins. 

The page is set to fill a 1920x1080 screen but can be scaled down in OBS. This is recommended as the current format takes up some reality. If you enjoy a large song box and need it to be smaller you can adjust the sizing on the body css itself.

The data from the SongStatusOutput.txt is written to a variable called SongData (very creative). If the SongStatusOutput.txt is empty (as such when in between active songs) the page will not display. This is achieved by the id bodyhide that can be applied to any parent DOM. Currently it is configured to the table. 

## Examples
![Cronosorich Song Overlay](https://i.imgur.com/3WlfpK4.png)

![WitchyRe Song Overlay](https://i.imgur.com/P1Rsp6T.png)

![Baelgor1979 Song Overlay](https://i.imgur.com/qyuzrRv.png)

## Future Enhancements
1. Standardize stylizing to allow easier customization.
2. Build easier interface for testing
3. Add instructions on how to integrate with OBS
