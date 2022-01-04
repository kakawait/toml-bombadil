<p align="center">
  <img
    width="250"
    src="./asset/logo.png"
    alt="Toml Bombadil - A dotfile manager written in rust"
  />
</p>

<p align="center">
  <a href="https://github.com/oknozor/toml-bombadil/actions"
    ><img
      src="https://github.com/oknozor/toml-bombadil/workflows/CI/badge.svg?branch=main"
      alt="GitHub Actions workflow status"
  /></a>
  <a href="https://codecov.io/gh/oknozor/toml-bombadil"
    ><img
      src="https://codecov.io/gh/oknozor/toml-bombadil/branch/main/graph/badge.svg"
      alt="Code coverage status"
  /></a>
    <a href="https://repology.org/project/bombadil/versions">
        <img src="https://repology.org/badge/version-for-repo/aur/bombadil.svg" alt="AUR package">
  </a>
  <br />
    <a href="https://crates.io/crates/toml-bombadil">
        <img src="https://img.shields.io/crates/v/toml-bombadil.svg" alt="crates">
  </a>
  <a href="https://conventionalcommits.org"
    ><img
      src="https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg"
      alt="Conventional commits"
  /></a>
  <a href="https://github.com/oknozor/toml-bombadil/blob/main/LICENSE"
    ><img
      src="https://img.shields.io/github/license/oknozor/toml-bombadil"
      alt="Repository license"
  /></a>
</p>

<p align="center">
  <a href="https://oknozor.github.io/toml-bombadil">Documentation</a>
  ·
  <a href="https://oknozor.github.io/toml-bombadil/docs/getting-started/quick-start/">Installation</a>
  ·
  <a href="https://docs.cocogitto.io/config">Configuration</a>
</p>

<h1></h1>

**A dotfile manager written in Rust**

- **Dotfile template:** define your dotfiles templates and link them as needed.
- **Dotfile profiles:** create profiles for different machines and situations and combine them on the flow.
- **Installation hooks:** run custom commands before and after installing your dotfiles.
- **Gpg encryption:** add encrypted secrets to your dotfile configuration with gpg.

<p align="center">
<a href="https://oknozor.github.io/toml-bombadil/docs/"><strong>Explore Toml Bombadil's docs&nbsp;&nbsp;▶</strong></a>
</p>


![example gif](asset/toml-bombadil.gif)

##  Why another dotfile manager ?

I wrote Toml Bombadil because I kept changing my desktop environment :
switching from i3 to sway, from sway to xfce, from xfce to gnome and back to sway.
When you keep changing your working environment like this you end up with several problems :
- Some symlinks will end up orphans.
- Not every program you use support Xresources and you will most probably have to manually edit some themes/config.
- When starting a fresh installation you will very likely need to adapt your existing dotfiles to your new machine.
- It is a mess

Toml Bombadil try to solve this with a simple addition to the symlink method used by other tools : instead of creating
a symlink from a dotfile to the actual config path of a program, it will create a copy of it and symlink the copy.
This additional step allow to use your original dotfile as a template and inject variables in the copy.
You can have multiple value files in the same dotfile repository and change color scheme, or any value on the fly.

In addition, this is completely optional, you could start using Toml Bombadil only to generate symlinks and templatize
your dot file progressively.

## Installation

**AUR:**
```bash
yay -S bombadil-bin
```

**Cargo:**
```bash
cargo install toml-bombadil
```

## Quickstart

See [Docs -> Quickstart](https://oknozor.github.io/toml-bombadil/docs/getting-started/quick-start/)

## Shell completions

Command line completion scripts for several popular shells can be generated by running `bombadil generate-completions`. An example for generating a completion script and outputting it to a file for zsh would be `bombadil generate-completions zsh > <somewhere on your $fpath>/_bombadil`. Available shells are: bash, elvish, fish, and zsh.

## Troubleshooting

If you get lost you can use `bombadil get {resource_name}` to see what is currently configured.
Available resources are `dots`, `hooks`, `path`, `profiles`, `vars`, `secrets`.

Optionally you can display resources for a profile with the `--profiles` flag.

## Example repositories

If you use Bombadil please submit an issue, or a PR to update this section, we will be happy to reference your dotfiles here !

- [https://github.com/oknozor/dotfiles](https://github.com/oknozor/dotfiles)
- [https://github.com/mrkajetanp/dotfiles](https://github.com/mrkajetanp/dotfiles)
- [https://github.com/HaoZeke/Dotfiles](https://github.com/HaoZeke/Dotfiles/tree/bombadil)
  
## Contributing

Found a bug, have a suggestion for a new feature ?
Please read the [contribution guideline](CONTRIBUTING.md) and submit an [issue](https://github.com/oknozor/toml-bombadil/issues).

## License

All the code in this repository is released under the MIT License, for more information take a look at the [LICENSE](LICENSE) file.



