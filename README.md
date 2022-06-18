# randomize-iterm-background
randomize your iTerm2 background color
iTerm2の背景色をランダムにセットします

## description
多数のターミナル画面を扱っているとき、背景色が適当に分散していると視覚的に作業しやすいです。そのように背景色をランダムに設定する機能がiTerm2になかったので作りました。

## synopsis
**randomize-iterm-background** [options]

## examples
```randomize-iterm-background```

iTerm2の背景色をランダムに設定します。
デフォルトでは濃い灰色 `#202020` に、RGB値それぞれ最大プラスマイナス8ずらした色が設定されます。

```randomize-iterm-background --background 808080 --amplitude FF0044 --animation-wait 0.1```

灰色 `#808080` から、Rを最大振れ幅255 (16進数でFF), Gを振れ幅なし, Bを最大振れ幅68 (16進数で44) で振動させた背景色に、純黒から0.1秒かけて設定します。

## options
**-b** RRGGBB, **--background** RRGGBB
: 背景色のベースを16進数で指定します。デフォルトは202020です。

**-a** RRGGBB, **--amplitude** RRGGBB
: 背景色への乱数振れ幅を16進数で指定します。デフォルトは101010です。

**--animation-wait** SECONDS
: 背景色の設定まで、漆黒から指定秒数かけて遷移します。無指定だと即座に設定します。

**-q**, **--quiet**
: エラーメッセージを一切表示しません。

## prerequisite
任意のruby実行環境で動くと思います。
ruby 2.6.8p205 arm64e-darwin21, ruby 3.0.3p157 arm64-darwin21, ruby 3.1.1p18 arm64-darwin21で動作確認できています。
依存外部パッケージはありません。

## license
Copyright (c) 2022 jun morimoto
Released under the MIT license
https://opensource.org/licenses/mit-license.php