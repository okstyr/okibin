# notes on my scan scripts

In order that they should probably be executed

## the rc file
`ln -s $PWD/scan-defaultrc $HOME/scan-defaultrc`
or if you just want to make local changes, do a `cp` instead

## scan-positioner
takes a quick scan and trims it to see if its positioned right
uses `convert` instead of `gm convert` so trimming may behave diffreently

## scan-photo
scans a photo

scans to 1200, does front first, then pauses so you can flip the image
takes a name as a param and writes output to raw/$name/$name_front.png etc

## scan-trim
trims white space

should be first step after scan-photo
takes same $name param as scan-photo
trims and outputs to trimmed/$name/$name_front.png etc

## scan-resize
NOTE - still needs productionising
takes a scan and resizes to a number of set sizes
should be next after scan-trim

note this is the size of the file - not the size of the image.
This seems to get much better results (in terms of file size) than multiple scans at different resolutions
and the output comparing low-res to low file size is actually better

## scan-borderise
experimental - adds a white border

