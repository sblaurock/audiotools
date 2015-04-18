audiotools
==========
Scripts to verify correctness of ID3 tags and sort mp3 files.

*Depends on Bash 4, id3info, id3v2.*

## audiosort

Verifies correctness of ID3 track information & moves mp3 files based on genre.

    audiosort [-f] directory

Script verifies that each track meets the following conditions:
* Genre, artist and title tag are present.
* Quality is 320kbps (sometimes buggy).
* "ft." (featuring) string is not located in artist tag (belongs in title).
* Words greater than three letters in length within genre, artist, album and title tags should begin with an uppercase letter.
* Genre, artist, album and title tags do not have double or trailing spaces.
* Filename matches the following tag structure: {artist} - {title}.mp3
* A folder exists in the output directory matching the value of the genre tag.

## audiolist

Outputs a sorted list of all artists, genres, albums or bitrates for mp3 files.

    audiolist directory tag
