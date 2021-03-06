# Vagrant 構築手順
- Vagrantのインストール
  ```
  sudo apt install vagrant
  ```
- vagrant-libvertのインストール
  ```
  # bulid-depのために必要
  sed -i 's/^# deb-src/deb-src/g' /etc/apt/source.list

  apt build-dep ruby-libvirt
  apt install qemu libvirt-bin ebtables dnsmasq
  apt install libxslt-dev libxml2-dev libvirt-dev zlib1g-dev ruby-dev

  # Vagrant 1.8はpluginインストールにバグがあるため暫定的な修正
  sed -i'' "s/Specification.all = nil/Specification.reset/" /usr/lib/ruby/vendor_ruby/vagrant/bundler.rb

  # vagrant-libvertのインストール
  sudo vagrant plugin install vagrant-libvert
  ```
- vagrant-mutateのインストール
  - boxファイルをKVM用に変換するプラグイン
  ```
  sudo vagrant plugin install vagrant-mutate
  ```

- 参考
  -  http://redj.hatenablog.com/entry/2016/12/16/004733
  -  https://github.com/vagrant-libvirt/vagrant-libvirt#installation
 
