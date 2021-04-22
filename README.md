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

Adding a new page:

1. create a new file `my-new-page.html` in root folder,

2. place the following contents into a file:
    ```
    ---
    layout: default
    ---
    ```
3. open `_config.yml` file, add a new item under `menu` list:

    ```
    - url: /my-new-page
      title: My new page
      enabled: true
    ```

4. Set `enabled: false` in case you don't want page to be visible yet,
5. Proceed with adding contents for new page

Adding contents for new page:

1. go to https://grid.layoutit.com,

2. make a grid as desired,

  * example: https://grid.layoutit.com/?id=uYNxeB7
3. copy-paste CSS and inner HTML (e.g. that _inside_ `<div class="grid-container">...</div>` container) into `my-new-page.html` file,
4. remove `grid-template-rows` CSS property from `grid-container` CSS selector,
5. rename `grid-container` CSS rule to `items`,
