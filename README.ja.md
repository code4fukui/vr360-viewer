# vr360-viewer

[A-Frame](https://aframe.io/) を使用して構築された、シンプルで埋め込み可能な360°写真ビューワーです。URLパラメータによる動的な画像の読み込みが可能で、iframeを使って任意のウェブページに簡単に組み込むことができます。

## 使い方

ビューワーを利用する主な方法は2つあります。

### 1. URLパラメータで画像を表示

`url`クエリパラメータを使用して、360°画像への直接リンクを指定します。

```
https://code4fukui.github.io/vr360-viewer/?url=[your-360-photo-url]
```

### 2. ウェブページに埋め込む

`<iframe>`を使用して、HTMLにビューワーを埋め込みます。ここでも`url`パラメータを使用できます。

```html
<!-- デフォルト画像で埋め込む -->
<iframe src="https://code4fukui.github.io/vr360-viewer/" style="width:100%;aspect-ratio:2/1;"></iframe>

<!-- 特定の画像で埋め込む -->
<iframe src="https://code4fukui.github.io/vr360-viewer/?url=img/fukuiit2023.jpg" style="width:100%;aspect-ratio:2/1;"></iframe>
```

## ギャラリー

このツールで表示可能な、さまざまなイベントの360°写真のコレクションです。

*   [2023-02-21 電脳メガネサミット2023](https://code4fukui.github.io/vr360-viewer/?url=img/sabaeit2023-1.jpg), [2](https://code4fukui.github.io/vr360-viewer/?url=img/sabaeit2023-2.jpg)
*   [2023-02-19 ふくいITエンジニア養成スクール at 福井産業支援センター](https://code4fukui.github.io/vr360-viewer/?url=img/fukuiit2023.jpg)
*   [2023-06-23 CyberFriday at 福井工大](https://code4fukui.github.io/vr360-viewer/?url=img/cyberfriday20230623-fut.jpg)
*   [2024-01-31 鈴鹿高専 スタートアップパネルディスカッション](https://code4fukui.github.io/vr360-viewer/?url=img/20240131-suzuka-kosen.jpg)
*   [2024-02-03 つくる、さばえ会議＆さばえまつり 懇親会](https://code4fukui.github.io/vr360-viewer/?url=img/20240203-sabae-matsuri.jpg)

その他の例については [list.html](https://code4fukui.github.io/vr360-viewer/list.html) をご覧ください。

## 高度な例

このリポジトリには、より複雑なシーンの例も含まれています。

*   **スライドショー**: [sbk.html](https://code4fukui.github.io/vr360-viewer/sbk.html) は、画像リストを自動的に切り替えるビューワーの例です。
*   **マルチスフィアシーン**: [cyberfriday.html](https://code4fukui.github.io/vr360-viewer/cyberfriday.html) は、`egxr.js` (Three.js) を使用して、軌道を描いて回転する複数の360°写真スフィア（球体）をレンダリングする例です。

## カスタムビューワーの作成

単一の静的な360°画像を表示する自己完結型のHTMLファイルを作成できます。

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
    <!-- rotation属性で初期ビューを設定 -->
    <a-sky src="./img/my-photo.jpg" rotation="0 -90 0"></a-sky>
  </a-scene>
</body>
</html>
```

## ライセンス

[MIT](LICENSE)
