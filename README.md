# Chilen PKGBUILD
> Fully offline, blazingly fast music player for your library

> [!NOTE]
> This is to be published on the AUR, but as of now account registration there is closed due to
> [supply-chain attacks](https://archlinux.org/news/active-aur-malicious-packages-incident/).

This repo contains the PKGBUILD file for building and installing the
[Chilen](https://github.com/tpaau/chilen) music player on Arch Linux. It is an official installation
method as stated in [Chilen's README](https://github.com/tpaau/chilen#installation).

The program installs as `chilen-git` so that it can be installed alongside a tagged release (which
would install as just `chilen`) should one be released.

> [!CAUTION]
> Chilen built from the `main` branch should only be used for development purposes or testing. I do
> not recommend you actually daily drive this as your music player until a tagged release is
> published. It won't do anything destructive, but do expect issues!

Please report strictly packaging-related issues
[here](https://github.com/tpaau/chilen-git-src-pkgbuild/issues/new), otherwise open an issue on the
[Chilen repo](https://github.com/tpaau/chilen/issues/new?type=bug).

## Usage
```git
git clone https://github.com/tpaau/chilen-git-src-pkgbuild
cd chilen-git-src-pkgbuild
makepkg -si
```
