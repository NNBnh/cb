<h1 align="center"><code>cb</code></h1>
<p align="center">Clipboard managers warper written in POSIX sh</p>
<p align="center"><img src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/twitter/281/clipboard_1f4cb.png" /></p>

## 💡 About

`cb` is a clipboard managers warper written in POSIX sh that wraps various system-specific tools for interacting with a system clipboard.
This is literally a port of [`clipboard.zsh` plugin](https://github.com/ohmyzsh/ohmyzsh/blob/master/lib/clipboard.zsh) from [Oh My Zsh](https://github.com/ohmyzsh) as a stand alone utility.

### ✨ Features

- Work with `tee` like pipeline (e.g: `ls | cb | grep -e 'string'`)
- Supported clipboard managers are:
  - `pbcopy`, `pbpaste`
  - `cygwin`
  - [`wl-clipboard`](https://github.com/bugaevc/wl-clipboard)
  - [`xclip`](https://github.com/astrand/xclip)
  - [`xsel`](http://www.kfish.org/software/xsel)
  - [`lemonade`](https://github.com/pocke/lemonade)
  - [`doitclient`](http://www.chiark.greenend.org.uk/~sgtatham/doit)
  - `win32yank`
  - [`termux-api`](https://wiki.termux.com/wiki/Termux:API)
  - [`tmux`](http://tmux.github.io)

## 📥 Installation

#### 🔧 Manually

```sh
curl https://codeberg.org/NNB/cb/raw/branch/main/bin/cb > ~/.local/bin/cb
chmod +x ~/.local/bin/cb
```

#### 📦 Package manager

For [Bpkg](https://github.com/bpkg/bpkg) user:

```sh
bpkg install NNBnh/cb
```

For [Basher](https://github.com/basherpm/basher) user:

```sh
basher install NNBnh/cb
```

> **Note** If you can and want to port `cb` to other package managers, feel free to do so.

## ⌨️ Usage

Copy `STRING` to clipboard:

```sh
cb STRING
```

```sh
echo STRING | cb
```

Copy file's data to clipboard:

```sh
cb < file.txt
```

Paste from clipboard:

```sh
cb
```

Pipe clipboard string to other tool:

```sh
cb | other-tool
```

## 💌 Credits

Special thanks to:
- [**clipboard.zsh**](https://github.com/ohmyzsh/ohmyzsh/blob/master/lib/clipboard.zsh) from [Oh My Zsh](https://github.com/ohmyzsh)

<a href="https://codeberg.org/NNB"><img width="100%" src="https://capsule-render.vercel.app/api?type=waving&section=footer&color=0284C7&fontColor=F0F9FF&height=128&desc=Made%20with%20%26lt;3%20by%20NNB&descAlignY=80" /></a>
