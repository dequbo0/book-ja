# Rust プログラミング言語

[![CircleCI](https://circleci.com/gh/rust-lang-ja/book-ja/tree/master-ja.svg?style=shield)](https://circleci.com/gh/rust-lang-ja/book-ja)

このリポジトリには「Rust プログラミング言語」の書籍のソースが含まれています。

[書籍は No Starch Press から紙の形式で入手可能です][nostarch]。

[nostarch]: https://nostarch.com/rust

また、オンラインで無料で読むこともできます。最新の [stable]、[beta]、または [nightly] Rust リリースに同梱されている書籍をご覧ください。これらのバージョンの問題は、更新頻度が低いため、このリポジトリですでに修正されている可能性があることにご注意ください。

[stable]: https://doc.rust-lang.org/stable/book/
[beta]: https://doc.rust-lang.org/beta/book/
[nightly]: https://doc.rust-lang.org/nightly/book/

書籍に掲載されているすべてのコードリストのコードのみをダウンロードするには、[releases] をご覧ください。

[releases]: https://github.com/rust-lang/book/releases

## 要件

書籍のビルドには [mdBook] が必要です。理想的には、rust-lang/rust が [このファイル][rust-mdbook] で使用しているものと同じバージョンを使用してください。入手するには：

[mdBook]: https://github.com/rust-lang-nursery/mdBook
[rust-mdbook]: https://github.com/rust-lang/rust/blob/master/src/tools/rustbook/Cargo.toml

```bash
$ cargo install mdbook --vers [バージョン番号]
```

## ビルド

書籍をビルドするには、次のように入力します：

```bash
$ mdbook build
```

出力は `book` サブディレクトリに生成されます。確認するには、ウェブブラウザで開いてください。

_Firefox:_
```bash
$ firefox book/index.html                       # Linux
$ open -a "Firefox" book/index.html             # OS X
$ Start-Process "firefox.exe" .\book\index.html # Windows (PowerShell)
$ start firefox.exe .\book\index.html           # Windows (Cmd)
```

_Chrome:_
```bash
$ google-chrome book/index.html                 # Linux
$ open -a "Google Chrome" book/index.html       # OS X
$ Start-Process "chrome.exe" .\book\index.html  # Windows (PowerShell)
$ start chrome.exe .\book\index.html            # Windows (Cmd)
```

テストを実行するには：

```bash
$ mdbook test
```

## 貢献

あなたの助けを歓迎します！私たちが求めている貢献の種類については、[CONTRIBUTING.md][contrib] をご覧ください。

[contrib]: https://github.com/rust-lang/book/blob/main/CONTRIBUTING.md

### 翻訳

書籍の翻訳にご協力いただけると嬉しいです！現在進行中の取り組みに参加するには、[Translations] ラベルをご覧ください。新しい言語の作業を開始するには、新しい issue を開いてください！複数言語対応の [mdbook サポート] を待っている状態ですが、開始は自由です！

[Translations]: https://github.com/rust-lang/book/issues?q=is%3Aopen+is%3Aissue+label%3ATranslations
[mdbook サポート]: https://github.com/rust-lang-nursery/mdBook/issues/5

## スペルチェック

ソースファイルのスペルエラーをスキャンするには、`spellcheck.sh` スクリプトを使用できます。有効な単語の辞書が必要で、これは `dictionary.txt` で提供されています。スクリプトが誤検出を生成した場合（例えば、スクリプトが無効と見なす `BTreeMap` という単語を使用した場合）、この単語を `dictionary.txt` に追加する必要があります（一貫性のためにソートされた順序を保持してください）。
