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
