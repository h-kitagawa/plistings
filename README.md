#`plistings` パッケージ

`plistings` パッケージは，`listings` パッケージを pLaTeX 上で用いる際の日本語対応処理を
強化するためのパッケージである．
[LuaTeX-ja](https://osdn.jp/projects/luatex-ja/wiki/FrontPage) 中の `lltjp-listings.sty` を
ベースとしている．

## 注意点（と，現在の制約）

* 実行には e-TeX 拡張が必要である（`\scantokens` 利用のため）．
  最近の TeX Live, W32TeX では `platex` と打つと標準で e-TeX 拡張が有効になっている．
* 内部で文字コード 0 の文字 (`^^@`, NUL) を日本語処理命令として用いている．
  そのため，NUL を含んだソースリストを出力することは出来なくなることに注意すること．
* 「LaTeX へのエスケープ」内では，和文文字を含んだ制御綴を使用することは出来ない．
