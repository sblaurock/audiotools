audiosort
=========

BASH script to validate and sort mp3 files into folders based on their genre.

    audiosort [-f] source

Requires id3info and id3v2 libraries.

Script verifies that each track meets the following conditions:
* Genre, artist and title tag are present.
* Quality is 320kbps (sometimes buggy).
* "ft." (featuring) string is not located in artist tag (belongs in title).
* Words greater than three letters in length within genre, artist, album and title tags should begin with an uppercase letter.
* Genre, artist, album and title tags do not have double or trailing spaces.
* Filename matches the following tag structure: {artist} - {title}.mp3
* A folder exists in the output directory matching the value of the genre tag.