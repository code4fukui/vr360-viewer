# vr360-viewer

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple, embeddable 360° photo viewer built with [A-Frame](https://aframe.io/). It allows for dynamic image loading via URL parameters and can be easily integrated into any webpage using an iframe.

## Usage

There are two primary ways to use the viewer.

### 1. View an Image via URL Parameter

Provide a direct link to a 360° image using the `url` query parameter.

```
https://code4fukui.github.io/vr360-viewer/?url=[your-360-photo-url]
```

### 2. Embed in a Webpage

Embed the viewer in your HTML using an `<iframe>`. You can also use the `url` parameter here.

```html
<!-- Embed with the default image -->
<iframe src="https://code4fukui.github.io/vr360-viewer/" style="width:100%;aspect-ratio:2/1;"></iframe>

<!-- Embed with a specific image -->
<iframe src="https://code4fukui.github.io/vr360-viewer/?url=img/fukuiit2023.jpg" style="width:100%;aspect-ratio:2/1;"></iframe>
```

## Gallery

A collection of 360° photos from various events, viewable with this tool.

*   [2023-02-21 電脳メガネサミット2023](https://code4fukui.github.io/vr360-viewer/?url=img/sabaeit2023-1.jpg), [2](https://code4fukui.github.io/vr360-viewer/?url=img/sabaeit2023-2.jpg)
*   [2023-02-19 ふくいITエンジニア養成スクール at 福井産業支援センター](https://code4fukui.github.io/vr360-viewer/?url=img/fukuiit2023.jpg)
*   [2023-06-23 CyberFriday at 福井工大](https://code4fukui.github.io/vr360-viewer/?url=img/cyberfriday20230623-fut.jpg)
*   [2024-01-31 鈴鹿高専 スタートアップパネルディスカッション](https://code4fukui.github.io/vr360-viewer/?url=img/20240131-suzuka-kosen.jpg)
*   [2024-02-03 つくる、さばえ会議＆さばえまつり 懇親会](https://code4fukui.github.io/vr360-viewer/?url=img/20240203-sabae-matsuri.jpg)

See [list.html](https://code4fukui.github.io/vr360-viewer/list.html) for more examples.

## Advanced Examples

This repository also contains examples of more complex scenes.

*   **Slideshow**: [sbk.html](https://code4fukui.github.io/vr360-viewer/sbk.html) demonstrates a viewer that automatically cycles through a list of images.
*   **Multi-Sphere Scene**: [cyberfriday.html](https://code4fukui.github.io/vr360-viewer/cyberfriday.html) uses `egxr.js` (Three.js) to render multiple, orbiting 360° photo spheres.

## Creating a Custom Viewer

You can create a self-contained HTML file to display a single, static 360° image.

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>My 360 Photo</title>
  <script src="https://code4fukui.github.io/aframe/dist/aframe-master.min.js"></script>
</head>
<body>
  <a-scene>
    <a-entity camera look-controls position="0 0 0"></a-entity>
    <!-- Set the initial view with the rotation attribute -->
    <a-sky src="./img/my-photo.jpg" rotation="0 -90 0"></a-sky>
  </a-scene>
</body>
</html>
```

## License

[MIT](LICENSE)