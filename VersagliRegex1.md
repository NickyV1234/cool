### convert movie data

find & replace `&amp;`


find left/right angle brackets didnt find...

find `^.+$` replace with `<movie>\0</movie>`

find `(<movie>)(.+?)\t`  replace with `\1<title>\2</title>`

find `(</title>)(.+?)\t` replace with `\1<date>\2</date>`

find `(</date>)(.+?)\t` replace with `\1<location>\2</location>`

find `(</location>)(.+?)(</movie>)` replace with `\1<time>\2</time>\3`

find `(<time)(>)(\d+) (min)` replace with `\1 unit="\4"\2\3`