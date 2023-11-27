# PKGBUILDs for mirakc
Arch LinuxにおいてDocker不要でmirakcをセットアップするPKGBUILD群

## バージョンについて
インストール時点での最新バージョンがビルドされます。

* mirakc-git
  ```release```ブランチより最新版を取得してビルドします。
* mirakc-arib-git
  ```main```ブランチより最新版を取得してビルドします。
  main上で作業中にインストールすると失敗する可能性があります。

注意: ```pkgver()```を持っているため、各PKGBUILDのバージョンが自動的に書き換わります。

## インストール
```bash
git clone https://github.com/haru3me/mirakc-PKGBUILDs.git
cd mirakc-PKGBUILDs/mirakc-arib-git
makepkg -si
cd ../mirakc-git
makepkg -si
```

```/etc/mirakc/config.yml```が設定ファイルなので、インストール後編集して下さい。

## systemdサービス
mirakc.serviceで操作できます。

```bash
systemctl enable --now mirakc.service
```
