# memo

## ファイルの10行目以降を表示する

- 方法：tail

```
tail -n +10 README.md
```
※ここが 10 行目。この行以降が表示されるはず。

- コメント

  検索すると、先頭 9 行は表示しないとか色々出てくるが、それだと入力が 9 なのか 10 なのかわかりにくいしそもそも読みづらい。

  とにかく簡潔に書く。

## git commit時に user.nameと user.email を指定する。

指定しないで git commit しようとすると、

> git config --global user.name "Your Name"
> git config --global user.email "you@example.com"

という出力が出る。コミットは出来ない。

git config --global してもよいが、他にたとえば以下の方法がある。

- 方法
  - git -c user.name='foobar' -c user.email='foobar@example.com' commit -m '...'
    - git commit 時に毎度指定が必要ではある。alias とかするとよいかも。
- 方法2
  ```
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  ```
  - これだと設定ファイルがどこかに作られた記憶がある。
- 方法3(?)
  - git config -- global で --global 無しで設定する。
