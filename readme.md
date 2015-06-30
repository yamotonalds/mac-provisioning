設定先で最初にやること
---
* コンピュータ名の設定
  `システムの環境設定` → `共有` → `コンピュータ名`
* リモートログインの設定
  `システムの環境設定` → `共有` → `リモートログイン` にチェック
  `システムの環境設定` → `共有` → `アクセスを許可` → `すべてのユーザ` を選択
* Xcodeのインストール
    ```sh
    sudo xcodebuild -license
    ```
* brew caskのインストール先設定
    ```sh
    echo 'export HOMEBREW_CASK_OPTS="--appdir=/Applications"' >> ~/.bash_profile
    ```

実行コマンド
---

```
ansible-playbook -i hosts --ask-pass --ask-sudo-pass base.yml
```

hostsファイルは以下の様なものを適当に用意する。

```txt:hosts
[mac]
juliet.local
```

その他
---

* Dashは？
    * AppStoreで購入したのでCaskでは入れない

