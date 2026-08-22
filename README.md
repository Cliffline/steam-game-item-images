# Steam Game Item Images

Public image host for Steam Inventory Service items in games published by **Cliffline Studios**.

Steam requires item icons to be served from a stable public URL. This repository stores those images and serves them through GitHub Pages, so item definitions can reference them directly.

## URL pattern

Base URL: <https://cliffline.github.io/steam-game-item-images>

```text
{base}/{game}/items/{item_id}/icon.png
{base}/{game}/items/{item_id}/large.png
```

## Directory rules

```text
{game}/items/{item_id}/icon.png
{game}/items/{item_id}/large.png
```

Game folders use lowercase kebab case. Item image file names are fixed as `icon.png` and `large.png`.

## Source images

Upload one source image per item:

```text
{game}/items-source/{item_id}.icon.png
```

GitHub Actions upscales each source and commits:

```text
{item_id}.icon.png -> {game}/items/{item_id}/icon.png   200x200
{item_id}.icon.png -> {game}/items/{item_id}/large.png  2048x2048
```

The source is scaled with its aspect ratio kept, so neither side exceeds the target size, then centered on a transparent canvas. Sources smaller than the target are enlarged by an integer factor with nearest-neighbor sampling to keep pixel edges sharp; oversized sources are downscaled with Lanczos.

## Games

- Bundoro

## Usage

The images belong to Cliffline Studios and are published here only so Steam and the games can load them. They are not offered for reuse in other projects.
