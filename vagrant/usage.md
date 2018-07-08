# Vagrant 覚書き
- ゲストOSの初期化
  ```
  vagrant init <box>
  ```
- ゲストOSの起動
  ```
  vagrant up <machine name>
  ```
- ゲストOSのssh
  ```
  vagrant ssh <machine name>
  ```
- boxの追加
  ```
  vagrant box add <URL or path>

  # bento/ubiuntu-16.04-i386からboxを追加
  vagrant box add bento/ubuntu-16.04-i386
  ```
- boxファイルをKVMで利用できる形式に変換
  ```
  vagrant mutate <name of file or url> --input-provider <provider> libvirt
  ```
- 参考
  - http://knowledge.sakura.ad.jp/2535/

