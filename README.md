# olma.github.io

In case we need to fetch images from Google in different sizes:
https://sites.google.com/site/picasaresources/Home/Picasa-FAQ/google-photos-1/how-to/how-to-get-a-direct-link-to-an-image

Status doc:
https://docs.google.com/spreadsheets/d/1M2m4Ctz-WYophsP0XDWRZa5glpApDyFfroOr4bAoP3E/edit#gid=0

Figma: https://www.figma.com/file/SqcawloYI1PxmyPeMyr5Ck/olga-antonova.net?node-id=1%3A39

In order to convert files run:

```fish
for i in (seq 1 19)
  cwebp -q 80 $i.jpg -o $i.webp
end
```

`80` is probably too small of a value.
