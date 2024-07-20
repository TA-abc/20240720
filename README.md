# memo

## ファイルの10行目以降を表示する

- 方法：tail

```
tail -n +10 README.md
```
ここが 10 行目。

## コメント

先頭 9 行は表示しない、とかあるがそれだと入力が 9 なのか 10 なのかわかりにくいので簡潔に書く。

## git commit時に user.nameと user.email を指定する。

指定しないで git commit しようとすると、
> git config --global user.name "Your Name"
> git config --global user.email "you@example.com"
が、他にたとえば以下の方法 1 がある。

- 方法1
  - git -c user.name='foobar' -c user.email='foobar@example.com' commit -m '...'
    - 都度指定が必要。alias とかするとよいかも。
- 方法2
  ```
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  ```
  - これだと設定ファイルがどこかに作られた記憶がある。
- 方法3(?)
  - git config -- global で --global 無しで設定する。
