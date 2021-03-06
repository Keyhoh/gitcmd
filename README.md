# gitcmd

git いじってて「欲しいなぁ」って思ったコマンドを作り投げるところ。

## 基本的な作り方

1. bash ファイルを用意する。
2. ファイル名にプレフィクス "git-" をつけて保存する。
3. path の通ったディレクトリに配置する。

## 使い方

1. プレフィクス "git-" を除いたファイル名で git コマンドを叩く。

## 仕様

* [git-hash](#git-hash)

---

## git-hash

### 概要

今いる branch のコミットログから、$1（第一引数）で始まるコミットハッシュを取得する。

#### 使用例

cherry-pick するときにコミットハッシュをコピペしなくて良い。

```cmd
$hash = git hash abc
git checkout develop/test
git cherry-pick $hash
```

#### 参考情報

* [Bash | 正規表現でマッチした文字列をキャプチャして使う](https://qiita.com/YumaInaura/items/b0f29b0061779e296068)
* [gitで特定のcommitバージョン/リビジョンを指すアレをなんと呼ぶか問題](https://qiita.com/bigwheel/items/0b331451558637ee29b3)
* [Bash $((算術式)) のすべて - A 基本編](https://qiita.com/akinomyoga/items/9761031c551d43307374)
* [シェルスクリプトでエラー時の処理を行う方法](https://qiita.com/sh19910711/items/db382a9da77e8ebbf041)
* [【bash】行ごとに処理する](https://qiita.com/kazu56/items/83340a2e284298b9e237)
* [シェルで文字列の長さを取得 (ただし、awkその他のプログラミング言語は無しでサクッと）](https://qiita.com/jun68ykt/items/3095b63cde309aff974d)
* [How can I test if a variable is empty or contains only spaces?](https://unix.stackexchange.com/questions/146942/how-can-i-test-if-a-variable-is-empty-or-contains-only-spaces)