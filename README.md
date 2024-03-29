# ![mvmake](https://user-images.githubusercontent.com/20663815/158886263-d3cd2695-6f28-457c-b1a3-5b342eebf818.png)

This script takes a music file and a directory of videos (clips) then creates a _music video_.

## Installation
The script is pypi available. You can install via pip.
```
python3 -m pip install mvmake
```

## Usage

### Simple example
```
mvmake --music ./my_new_song.wav --clips ./path/to/clips my_music_video.mp4
```

### Help output
```
$ mvmake --help

usage: mvmake [-h] --music MUSIC --clips CLIPS [--extensions EXTENSIONS]
              [--method [{onset,beat,union}]] [--width WIDTH]
              [--height HEIGHT]
              output

Snap some clips to music. This script takes an audio file and a directory
where video clips are located then tries to match the given clips to the given
audio.

positional arguments:
  output                The name of the output file.

optional arguments:
  -h, --help            show this help message and exit
  --music MUSIC         Path to the music file.
  --clips CLIPS         Path to the directory containing the clips. All the
                        clips will be read from the directory recursively.
  --extensions EXTENSIONS
                        The enabled extensions of the clips. Files with other
                        extensions will not be used. (default: ['mp4', 'avi',
                        'mov'])
  --method [{onset,beat,union}]
                        Select to what to snap the clips. Currently there are
                        three methods supported: onset (snap clips to the
                        starting of each note), beat (snap clips to each
                        beat), union (snap clips to both of these) (default:
                        onset)
  --width WIDTH         The width of the output. If given without height, the
                        clips aspect ratio will be kept. (default: None)
  --height HEIGHT       The height of the output. If given without width, the
                        clips aspect ratio will be kept. (default: None)
```

## Samples

### Sample 1: _Fall In Love_
This sample is constructed from ___DigEx - Fall In Love___ and clips from ___Beeple-Crap - übersketch___.  
The default ___onset___ detection method was used. (`--method onset`)

https://user-images.githubusercontent.com/20663815/158896029-0c74840e-c5bd-4fcd-89ad-8f33d66c8ace.mp4

#### Licenses
```
Song: DigEx - Fall In Love [NCS Release]
Music provided by NoCopyrightSounds
Free Download/Stream: http://NCS.io/FallInLove
Watch: http://youtu.be/

VJ Loops: Beeple-Crap - übersketch
https://www.beeple-crap.com/vjloops
```
### Sample 2: _Talk_
This sample is constructed from ___Beave - Talk___ and clips from ___Beeple-Crap - four.color.process___.  
The ___beat___ detection method was used. (`--method beat`)

https://user-images.githubusercontent.com/20663815/158896309-87955912-f3b9-47c1-9c2e-a29a9b80ef51.mp4

#### Licenses
```
Song: Beave - Talk [NCS Release]
Music provided by NoCopyrightSounds
Free Download/Stream: https://ncs.io/Talk
Watch: https://youtu.be/uZi8_rnqgHg

VJ Loops: Beeple-Crap - four.color.process
https://www.beeple-crap.com/vjloops
```

## Changelog

[Learn about the latest improvements](CHANGELOG.md).

## Contributing

### Contributing Guidelines

Read through our [contributing guidelines](CONTRIBUTING.md) to learn about our submission process, coding rules and more.

### Want to Help?

Want to report a bug, contribute some code, or improve documentation? Excellent! Read up on our guidelines for [contributing](CONTRIBUTING.md) and then check out one of our issues labeled as <kbd>[help wanted](https://github.com/kenyerman/mvmake/labels/help%20wanted)</kbd> or <kbd>[good first issue](https://github.com/kenyerman/mvmake/labels/good%20first%20issue)</kbd>.

## License

The project is licensed under MIT License. Read more [here](LICENSE).

## Shoutout to these guys 🎉💖
This project is based on the following packages, check them out!

 - [MoviePy](https://github.com/Zulko/moviepy)
 - [librosa](https://github.com/librosa/librosa)
