<b> Some example usage of `convert` command </b>


To convert a file from a jpg to a pdf: `convert fileold.jpg filenew.pdf`

To resize an image to a fixed width and proportional height: `convert fileold.jpg -resize 100x filenew.jpg`

To resize an image to a fixed height and proportional width: `convert file old.jpg -resize x100 filenew.jpg`

To resize an image to a fixed width and height: `convert fileold.jpg -resize 100x100 filenew.jpg`

To resize an image and simultaneously change its file type: 
```js
convert fileold.jpg -resize 100x filenew.png`
```

To resize all of the images within a directory:
```js
for file in `ls original/image/path/`;
    do new_path=${file%.*};
    new_file=`basename $new_path`;
    convert $file -resize 150 converted/image/path/$new_file.png;
done
```

To convert an N page pdf to N images (autonumbering): `convert -density 150 fileoriginal.pdf -quality 80 'outputfile.jpg'

To convert an N page pdf to N images with explicit filename formatting:
```js
convert -density 150 fileoriginal.pdf -quality 80 'outputfile-%d.jpg'
```
