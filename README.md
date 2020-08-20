# 開発者に適した VSCode ポータブル版の導入方法
VSCode ポータブル版のインストール方法を説明する。対象 OS は Windows 10 です。

## OS のビット数の確認
自分の Windows が 64 ビット対応か、32 ビット対応かを確認する。

コマンドプロンプトで次のコマンドを実行すると、ビット数が分かる。
```console
systeminfo
```
実行結果例: 
```
ホスト名:               NPWE41
OS 名:                  Microsoft Windows 10 Home
OS バージョン:          10.0.18363 N/A ビルド 18363
...
システムの種類:         x64-based PC
```

「システムの種類」が `x64-based PC` なら 64 ビット OS で、`x86-based PC` なら 32 ビット OS となる。

## 本体 Zip ファイルのダウンロード
以下の公式ページよりダウンロードする。

Download Visual Studio Code - Mac, Linux, Windows  
[https://code.visualstudio.com/download](https://code.visualstudio.com/download)

ページを見ると、以下のようにインストーラの種類が揃っている。この中から「.zip」のインストーラを自分の OS のビット数に応じてダウンロードする。
<table>
  <tr>
    <td>User Installer</td>
    <td>64 bit</td>
    <td>32 bit</td>
    <td>ARM</td>
  </tr>
  <tr>
    <td>System Installer</td>
    <td>64 bit</td>
    <td>32 bit</td>
    <td>ARM</td>
  </tr>
  <tr>
    <td><strong>.zip</strong></td>
    <td>64 bit</td>
    <td>32 bit</td>
    <td>ARM</td>
  </tr>
</table>

## Zip ファイルの解凍
例えば、64 ビットだったら `VSCode-win32-x64-1.41.1.zip` というファイルがダウンロードできる。

このファイルを解凍する。中身のフォルダ・ファイルは以下の通りになっている。

```
C:\VSCode-win32-x64-1.41.1.zip
├─bin
├─ locales
├─ resources
├─ swiftshader
├─ tools
│  chrome_100_percent.pak
│  chrome_200_percent.pak
│  Code.exe
│  Code.VisualElementsManifest.xml
│  d3dcompiler_47.dll
│  ffmpeg.dll
│  icudtl.dat
│  libEGL.dll
│  libGLESv2.dll
│  natives_blob.bin
│  resources.pak
│  snapshot_blob.bin
└─ v8_context_snapshot.bin
```

この中の `Code.exe` が実行ファイルで、この .exe ファイルを実行すれば VSCode を起動することができる。

実際に VSCode を起動する前に、ユーザ設定データを格納する場所を、以下の手順で作る。

## data フォルダの作成
上記の解凍したフォルダ内に 'data' という名前のフォルダを作成する。中身は空でよい。

VSCode を使っていく中で利用していくプラグイン（Extention: 拡張機能）や設定情報は、この作成した'data' フォルダの中に保存されていく。

つまり、この 'data' フォルダさえあれば、どの PC だろうと、Zip を解凍した VSCode のフォルダ内に放り込むことで、今まで通りの自分の設定で VSCode が瞬時に使えるようになる・・・という仕組みだ。

だから、持ち運びができる「ポータブル版」というわけだ。

USB に、この VSCode フォルダを入れて、PC にそのまま USB を挿してアプリを起動することもできる。

カンタンに自分の設定や環境を移動できるという点で、ポータブル版は開発者に向いている仕組みだ。

## VSCode フォルダの置き場
出来上がった VSCode フォルダは、どこに置いても良い。

C: ドライブ直下などに置いても、アプリの動作には問題ない。

フォルダの名前は、自分の好きなようにリネームしても構わない。

