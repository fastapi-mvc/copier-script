## Copier Script

Copier template for scaffolding new script upon [fastapi-mvc](https://github.com/fastapi-mvc/fastapi-mvc) project.

## Quickstart

### Using fastapi-mvc

Prerequisites:
* fastapi-mvc
* Git 2.27 or newer

```shell
git clone "https://github.com/fastapi-mvc/copier-script.git"
FMVC_PATH="$PWD:$FMVC_PATH" fastapi-mvc generate script /path/to/your/new/script
```

### Using copier

To use this template outside `fastapi-mvc`:

Prerequisites:

* Python 3.8 or later [How to install python](https://docs.python-guide.org/starting/installation)
* Git 2.27 or newer
* copier 6.2.0 or later

```shell
copier copy "https://github.com/fastapi-mvc/copier-script.git" /path/to/your/new/script
```

## Using Nix

Prerequisites:

* Nix 2.8.x or later installed [How to install Nix](https://nixos.org/download.html)

```shell
nix develop
copier copy "https://github.com/fastapi-mvc/copier-script.git" /path/to/your/new/script
```

## Updating

To update your generator with the changes from the [upstream](https://github.com/fastapi-mvc/copier-generator) run:

```shell
./update.sh
# Or
nix run .#update
```

This action will not update/override your template and its configuration, but rather generators common files:

* Nix expression files
* `README.md`
* dotfiles
* `LICENSE`

List of excluded files/paths:

* `template/**`
* `copier.yml`
* `*.py`
* `CHANGELOG.md`

Lastly, you can pass extra copier CLI options should you choose:

```shell
./update.sh -x README.md --vcs-ref=custom_branch
# Or
nix run .#update -- -x README.md --vcs-ref=custom_branch
```
