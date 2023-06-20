# Notes while learning rust

---

## Notes from NoBoilerPlate Video

Link: <https://github.com/0atman/noboilerplate>
<https://www.youtube.com/watch?v=2hXNd6x9sZs>

Book: <https://doc.rust-lang.org/stable/book/>

The Book <https://doc.rust-lang.org/stable/book/>

Everything on fasterthanli.me, starting with <https://fasterthanli.me/articles/understanding-rust-futures-by-going-way-too-deep>

Rust By Example (follows the same chapter ordering to The Book) <https://doc.rust-lang.org/rust-by-example/>

Rustlings code kata, learn by fixing tiny failing tests <https://github.com/rust-lang/rustlings>

My video series on Rust (of course!) playlist here, watch RUST-6 first (my recommended set up) and then the rest in any order: <https://www.youtube.com/watch?v=ifaLk5v3W90&list=PLZaoyhMXgBzoM9bfb5pyUOT3zjnaDdSEP&index=6>

My Discord server, especially #programming and #newbie-advice. There's a huge community of friendly folks here, answering questions on Rust all day every day. Do tag me and say hi! <https://discord.gg/mCY2bBmDKZ>

Have fun, and good luck!

---

## Machine Setup

* If windows... get wsl2 with fedora setup.
  * <https://www.linuxfordevices.com/tutorials/linux/install-fedora-on-windows>
* Set up visual studio code on host machine with wsl2 plugin
  * rust-analyzer
  * rust syntax (maybe?! not sure if needed)
  * crates
  * even better toml
* Install other extensions into wsl2 instance
* `sudo dnf install git-all`
* cd into a location where repos are kept
* `git clone https://github.com/ambaumann/learning-rust-core.git`
* Configure shell... zsh and oh-my-zish looks pretty good
  * `sudo dnf install zsh`
  * launch and configure zsh default settings by typing 'zsh'
  * Default zsh
    * `sudo dnf install util-linux-user` for chsh
    * `chsh -s $(which zsh)`
  * `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
  * change default terminal in vs code to zsh

* <https://www.rust-lang.org/tools/install>
* `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
* `source "$HOME/.cargo/env"`
* `vi ~/.zshrc` and update alias for zshconfig, ohmyzsh and add rustup env above
* source new changes with `zsh`
* `sudo dnf groupinstall "Development Tools"`
* `sudo dnf install openssl`
* `sudo dnf install pkg-config openssl-devel`
* Clone my rustlings project for now.
  * From repos directory `git clone https://github.com/ambaumann/rustlings-solution.git`
  * `cd ./rustlings-solution`
  * `code -n .`
  * `git checkout first-go`
  * `./install.sh` from project directory
  * `rustlings lsp` for generating the editor lsp config
  * Validate that the rust-analyzer is running
    * I needed to add: `rustup component add rust-src`
    * <https://github.com/rust-lang/rust-analyzer/issues/11606>
  * `rustlings watch`

---

Rustlings

Pretty easy to set up. Make sure you open in own project in vs code and run rustlings lsp.

---

## Golang

Install instructions:

* Go to <https://go.dev/doc/install>
* Install instructions are there. It is a bit annoying to set up in WSL.
* I put the install into XYZ
* `tar -C /usr/local -xzf go1.20.5.linux-amd64.tar.gz`
* To .zshrc: `export PATH=$PATH:/usr/local/go/bin`

VS Code Go Extensions

* Install Go extension
  * If you see `The "gopls" command is not available. Run "go install -v golang.org/x/tools/gopls@latest" to install.`
    Hit "Install ALL" if prompted by VS Code.
  * <https://stackoverflow.com/questions/66668506/how-to-solve-vs-code-gopls-command-is-not-available>
  * Installing 7 tools at /home/andrew/go/bin in module mode.
    * gotests
    * gomodifytags
    * impl
    * goplay
    * dlv
    * staticcheck
    * gopls
* go-outliner (install go modules it uses)

---

## Exercism

* Instructions at: <https://exercism.org/cli-walkthrough>
* Select Linux
* Download release from: <https://github.com/exercism/cli/releases>
* unpack with `tar -xf ./exercism-3.1.0-linux-x86_64.tar.gz`
* `mkdir -p ~/bin`
* `mv ./exercism ~/bin`
* test with `~/bin/exercism`
* test if exercism is in path `[[ ":$PATH:" == *":$HOME/bin:"* || ":$PATH:" == *":~/bin:"* ]] && echo "~/bin is in PATH" || echo "~/bin is not in PATH"`
* if it isn't, modify .zshrc with 'export PATH=~/bin:$PATH'
* set your exercism token with instructions from the website `exercism configure --token=....`
* you should be ready to download exercises! Example `exercism download --exercise=blackjack --track=go`
