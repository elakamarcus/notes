# Install MS VS Code on debian/ubuntu (apt)

## Prerequisit

### Required packages
Install support for fetching https repositories (ie. the first part of the guide: [Here](https://github.com/elakamarcus/notes/blob/master/debian_ubuntu_secureupdates.md) )
Additionally, unless you have wget installed already:
``` sudo apt update ``` \
followed by \
``` sudo apt install wget ```

### Fetch GPG keys

```
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
```

## Add and enable the repository

```
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
```

## Install MS VS Code
```
sudo apt update
sudo apt install code
```

## Test
```bash
$ code
```

Enjoy
