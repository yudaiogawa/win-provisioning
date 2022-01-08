


# Setup Win

Windows no setup wok ait ekini :)

<br>

## ZSH

Install zshell:

```shell
sudo apt-get install zsh
```

- Switch default shell to zsh.
- Create .zshrc using dotfile repository.

<br>

## Create SSH Key

Setup:

```sh
mkdir ~/.ssh
mkdir ~/.ssh/$service
touch ~/.ssh/config
```

Create SSH key:

```sh
ssh-keygen -t rsa -b 4096 -f ~/.ssh/$service/id_rsa -C alice@example.com
```

Register a following result to service:

```sh
cat ~/.ssh/$service/id_rsa.pub
```

`~/.ssh/config` に以下内容を記述。

```sh
Host foobar
  User git
  Hostname $service_domain
  identityFile ~/.ssh/$service/id_rsa
```

<br>

## Change Key layouts

`Caps Lock` と `Ctrl` のキーを交換する。
`regedit.exe` を使用して、レジストリを書き換える。クリティカルな作業なので気を付けてね。

<br>

## Change Policy

管理者権限で `PowerShell` を起動し、以下コマンド実行。

```sh
> Set-ExecutionPolicy RemoteSigned
```

- `RemoteSigned`
  - ローカルで作成されたスクリプトは無条件で実行可能だが、外から入手したスクリプトは、署名が無ければ実行不可

<br>

## Install Apps

- Choco or Scoop or etc.
- Google Chrome
- Bitwarden
- Evernote
- Discord
- Dropbox
- IntelliJ IDEA
- Visual Studio Code
- ScreenToGif
- Slack
- Zoom
- DeepL
- [Cmder](https://cmder.net/)

<br>

## Install Cmder

Install binary from [Cmder](https://cmder.net/). Unzip result to C drive.

#### Settings

デフォルトで、WSL環境をターミナルできるように設定する。

Change home directory in cmder to WSL home directory:

```sh
-new_console:d://wsl$/Ubuntu/home/yudaiogawa
```

Makeup the appearance :)

<br>

## VScode

Install the extensions.

```shell
# theme
code --install-extension sainnhe.gruvbox-material
code --install-extension pkief.material-icon-theme
# wabisabi
code --install-extension MS-CEINTL.vscode-language-pack-ja
# Remote-SSH, etc.
code --install-extension ms-vscode-remote.vscode-remote-extensionpack
# git
code --install-extension eamodio.gitlens
code --install-extension donjayamanne.githistory
# Docker
code --install-extension ms-azuretools.vscode-docker
# linter
code --install-extension dbaeumer.vscode-eslint
code --install-extension DavidAnson.vscode-markdownlint
# formatter
code --install-extension nmrmsys.vscode-sql-formatter-mo
# prettier
code --install-extension esbenp.prettier-vscode
code --install-extension eriklynd.json-tools
code --install-extension bierner.github-markdown-preview
# Debug javascript
code --install-extension msjsdiag.debugger-for-chrome
# YAML
code --install-extension redhat.vscode-yaml
# TODO comment
code --install-extension gruntfuggly.todo-tree
# json2csv n csv2json
code --install-extension khaeransori.json2csv
```



