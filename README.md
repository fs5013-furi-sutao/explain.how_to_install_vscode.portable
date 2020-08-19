# 
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
