


# Setup WSL

Windows subsystem 4 linux wo setup sit eiku :)

<br>

## Setup WSL & Dev tools

WSL2導入および開発ツールをセットアップする。

「コントロールパネル > プログラムと機能 > Windowsの機能の有効化または無効化」を開き、以下の項目を有効化。

- Hyper-V
  - もしかしたら off でいいかも
- Linux用Windowsサブシステム
- 仮想マシンプラットフォーム

MS公式の [WSLの開発環境を設定する](https://docs.microsoft.com/ja-jp/windows/wsl/setup/environment) を参考に以下を完了させる。

- WSLの導入
- 開発ツールのセットアップ
  - Visual Studio Code のセットアップ
  - Git のセットアップ

WSLのバージョンが2であることを確認する。

```sh
wsl -l -v
```

WSL環境の日本語化

```sh
# Install package
sudo apt -y install language-pack-ja
# Change locale
sudo update-locale LANG=ja_JP.UTF8
# Change timezone
sudo dpkg-reconfigure tzdata
# Check timezone
date
```

<br>

## Setup Docker

Docker環境を構築する。

#### Install Docker Engine

[Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/) を参考にインストールする。
Docker公式がおすすめしている方法でインストールする。

#### Install Docker Compose

[Install Docker Compose](https://docs.docker.com/compose/install/) を参考にインストール。

<br>

## Create SSH key

refs. [Create SSH key](./setup-win.md#create-ssh-key)
