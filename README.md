# CBoxToGo

Command-line tool for downloading series/episodes from China Network Television (CNTV), based on reverse engineering of [CBox](http://cbox.cntv.cn/)

## Requirements

* Python 3.2+
* requests
* ffmpeg, wget in system path

## Usage

```
$ python CBoxToGo.py --help
usage: CBoxToGo.py [-h] [-s S] [-l L] videoset_id output_dir

positional arguments:
  videoset_id  Videoset ID of the series (vsetid attributes in playlist.json)
  output_dir   Output directory of downloaded episodes

optional arguments:
  -h, --help   show this help message and exit
  -s S         comma-separated list of episodes and/or ranges to download,
               e.g. 1,2,4-8
  -l L         download rate limit, passed to wget --limit-rate=
 
```

## How to find the Videoset ID

1. Open [playlist.json](playlist.json) in a text editor.
2. Search for the name of your show.
3. Find the corresponding `vsetid` value.

For example, the videoset ID of the show 《打狗棍》 is `VSET100174517074`.

## Known issues/limitations

* Unicode characters are not displayed correctly in Windows command prompts.

## Support

Please use the GitHub Issue Tracker and pull request system to report bugs/issues and submit improvements/changes, respectively.  