# iOS Cheat Decrypter

## 概要
iOSのModMenu、Tweak系のチートでどこを改変しているのかを出力するアプリです。  
[作者 @ykm_s_labo](https://x.com/ykm_s_labo)
<br>
<br>

## インストール  
[Release](https://github.com/DFuku/iOS-Cheat-Decrypter/releases/tag/v0.0.1)から自身の環境にあったバージョンをダウンロードし、FilzaかSileo等でインストールしてください。  
\(rootful = iphoneos-arm\)  
\(rootless = iphoneos-arm64\)  
\(roothide,bootstrap = iphoneos-arm64e\)  

## 使い方
インストール後、Filzaで  
```/Library/MobileSubstrate/DynamicLibraries/!!!!!cheatdecrypter.plist```  
に適用したいアプリのbundleIDを追加してください。  
例としてツムツムのbundleIDは最初から追加してありますので、それを参考に追加してください。  
<br>
また、rootlessの場合上記パスではなく  
```/var/jb/~~~```  
で、roothide、bootstrapの場合  
```/var/containers/Bundles/.jbroot[ランダムな英数字]/~~~```  
となります。
<br>
<br>
適用できたら該当アプリを起動し、起動後約12秒後に画面左上にダイヤのマークが出ます。（出ない場合plistが間違ってる可能性があります）  
<br>
その後、解析したいチートをONにし、ダイヤマークをタップして左上のScanボタンを押せば解析結果が画面に表示されます。  
<br>
見つからない、あるいはバイナリ改変ではない場合not foundと表示されます。

## 注意
予め改変されたバイナリをアプリのバイナリと置き換える手法には対応していません。あくまで正規のバイナリを起動後改変するタイプのみに対応しています。
