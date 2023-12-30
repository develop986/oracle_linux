# oracle_linux
Oracle Linux での各種マニュアル

## OSインストール

- https://yum.oracle.com/oracle-linux-isos.html
  - https://yum.oracle.com/ISOS/OracleLinux/OL9/u3/x86_64/OracleLinux-R9-U3-x86_64-dvd.iso

- VirtualBoxでの構築
  - ![VirtualBox](./img/VirtualBox.png)

## 初期設定

1. 最初の諸々の設定
  ```
  $ sudo dnf -y install oracle-epel-release-el9
  $ sudo dnf -y install firewall-config
  $ sudo dnf -y install git
  $ git config --global user.email "kuhataku@gmail.com"
  $ git config --global user.name "kuhataku"
  $ sudo grubby --update-kernel ALL --args selinux=0
  $ sudo reboot
  ```

2. 日本語入力（再起動が必要）
  - ![JapaneseLanguage](./img/JapaneseLanguage.png)

3. リモートデスクトップ接続設定
  ```
  $ sudo dnf -y install xrdp tigervnc-server
  $ sudo systemctl start xrdp
  $ sudo systemctl enable xrdp
  $ sudo reboot
  ```
  - ![Firewall](./img/Firewall.png)



