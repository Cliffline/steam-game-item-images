# Steam Game Item Images

This repository hosts publicly accessible item images for Steam games.

## URL pattern

```text
https://YOUR_USERNAME.github.io/steam-game-item-images/{game}/items/{item_id}/icon.png
https://YOUR_USERNAME.github.io/steam-game-item-images/{game}/items/{item_id}/large.png
```

## Directory rules

```text
{game}/items/{item_id}/icon.png
{game}/items/{item_id}/large.png
```

Game folders use lowercase kebab case. Item image file names are fixed as `icon.png` and `large.png`.

## Source images

Upload source images next to the generated files:

```text
{game}/items/{item_id}/source-icon.png
{game}/items/{item_id}/source-large.png
```

GitHub Actions pads them with transparent margins and commits:

```text
source-icon.png  -> icon.png  200x200
source-large.png -> large.png 2048x2048
```

The image content is centered and not scaled.

## Current games

- Bundoro
