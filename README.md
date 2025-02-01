# Debian Repository for LoongArch64

This repository provides Debian packages specifically built for LoongArch64(linux/loong64) architecture. You can find all packages here: https://github.com/loong64/repo/commits/master

All packages in this repository are compiled and optimized for LoongArch64.

## Package List

| Package Name              | Install Command                              | Description                                    |
| ------------------------- | -------------------------------------------- | ---------------------------------------------- |
| gh                        | `sudo apt install gh`                        | GitHub's official command line tool            |
| containerd.io             | `sudo apt install containerd.io`             | An open and reliable container runtime         |
| docker-buildx-plugin      | `sudo apt install docker-buildx-plugin`      | Docker Buildx CLI plugin                       |
| docker-ce                 | `sudo apt install docker-ce`                 | Docker Engine                                  |
| docker-ce-cli             | `sudo apt install docker-ce-cli`             | Docker CLI                                     |
| docker-ce-rootless-extras | `sudo apt install docker-ce-rootless-extras` | Rootless support for Docker                    |
| docker-compose-plugin     | `sudo apt install docker-compose-plugin`     | Docker Compose (V2) plugin for the Docker CLI  |

### Repository Installation

```sh
# Add GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl

sudo curl -fsSL "https://loong64.github.io/repo/debian/debian-loong64-archive-keyring.gpg" -o /usr/share/keyrings/debian-loong64-archive-keyring.gpg
sudo chmod a+r /usr/share/keyrings/debian-loong64-archive-keyring.gpg

# Add repository:
echo \
  "deb [arch=loong64 signed-by=/usr/share/keyrings/debian-loong64-archive-keyring.gpg] https://loong64.github.io/repo/debian trixie main" | \
  sudo tee /etc/apt/sources.list.d/debian-loong64-repo.list > /dev/null

# Install packages:
sudo apt update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

If you don't want to add this repository, you can directly download and install the loong64 deb packages from [here](https://github.com/loong64/repo/tree/master/debian).