# github.com/anthonygrimes/dotfiles

My dotfiles, managed with [chezmoi](https://www.chezmoi.io).

## Getting started

This project will manage the following:
- zsh
- git config
- ssh config
- 1Password ssh key vault

### Prerequisites

This project makes use of [templating](https://www.chezmoi.io/user-guide/templating/) and requires that some data be provided before you are able to apply your changes.

This can be done within your `~/.config/chezmoi/chezmoi.toml` file where the contents resembles:

```
[data.git]
    name = ""
    email = ""
    signingkey = ""
```

### Initialise, inspect and apply

To get started using my dotfiles you can run the following:

```shell
chezmoi init anthonygrimes
```

To inspect the changes you can run the following:

```shell
chezmoi diff
```

If you're happy with the changes you can run the following to apply the changes:

```shell
chezmoi apply
```

## Usage

For full usage information, please always consult the [official docs](https://www.chezmoi.io).

### Adding a new file to manage

To add new files for chezmoi to manage you can run the following:

```shell
chezmoi add ~/{file_to_manage}
```

### Editing a file under management

To edit a file that chezmoi manages you can run the following:

```shell
chezmoi edit ~/{file_to_manage}
```

You may optionally navigate to the chezmoi source directory and edit the file directly, to do so you can run the following:

```shell
chezmoi cd

// whatever commands you wish to make changes, or open in editor of choice
```

### Applying changes

To apply changes for files which have changed you can run the following:

```shell
chezmoi apply
```

### Seeing what is managed with Chezmoi

To see what chezmoi is managing you can run the following:

```shell
chezmoi managed
```

