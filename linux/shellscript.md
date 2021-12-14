## 変数のデフォルト値

[これ](https://qiita.com/minanon/items/d3c7dd0a74ea4f455551)を見れば OK
コロンがある場合は人目で見たときに値があるかどうか、コロンなしは変数自体が定義されているかを見る

```
hoge=1
echo ${hoge:+fuga} # 変数に１文字でも含まれていたら代入
# fuga
echo ${hoge+fuga} # 変数が定義されていたら代入
# fuga
echo ${fuga+empty} # 定義されていないので空文字列
# ""
echo ${hoge:-hoge} # 値が見えなければ代入
# 1
echo ${piyo-piyo} # 変数が未定義なら代入
# piyo
```
