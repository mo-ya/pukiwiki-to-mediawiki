==============================================
 Pukiwiki ドキュメントの MediaWiki 変換ツール
==============================================

使い方
======

Pukiwiki 形式のテキスト `~/Document.pukiwiki` を `~/Document.mediawiki` に変換する場合は以下のように利用。 ::

    $ cat ~/Document.pukiwiki | sed -z -f pukiwiki-to-mediawiki.sed > ~/Document.mediawiki


対応項目
============

- 見出し
- リスト
- 整形済みテキスト
- 表 (※ シンプルなパターンのみ。rowspan, colspan は未対応)
- Pukiwiki の見出しに含まれる [#xxxxxxxx] という文字列の削除
  
非対応項目
==========

- rowspan, colspan を含む表

動作確認環境
============

GNU sed 4.2.2

※ 特に -z オプションを利用しているため 4.2.1 以前では利用不可
