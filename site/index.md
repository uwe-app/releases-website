+++
title = "Software Releases"
+++

# {{title}}

Software releases for the [UWE][] platform tools.

## Quick Install

To install the latest release run:

```
curl https://releases.uwe.app/install.sh | sh
```

Get the [source code](https://github.com/uwe-app/releases/blob/main/install.sh) for the [quick install script](https://releases.uwe.app/install.sh).

## Upgrade

After installation to update to the latest version run:

```
uvm update
```

## Manual Install

If you prefer to avoid piping to `sh` then the manual installation steps are shown below; use the URL appropriate for your platform.

* Linux: `https://releases.uwe.app/latest/linux/uvm`.
* Macos: `https://releases.uwe.app/latest/macos/uvm`.

```
mkdir -p $HOME/.uwe/bin && cd $HOME/.uwe/bin
curl -OL --fail --progress-bar "https://releases.uwe.app/latest/linux/uvm"
chmod +x ./uvm && ./uvm update
```

## Checksums

The checksums listed here are `SHA3-256` digests.

To compute the digest for a file on Linux use `sha3sum`, for debian-based distributions `sha3sum` is available in the package `libdigest-sha3-perl`:

```
sha3sum -a 256 uvm
```

On MacOs use `shasum`:

```
shasum -a 256 uvm
```

{{#with result.[0]}}

{{#with this.value.latest}}
## Latest {{this.version}}
{{#if this.published}}
<small>Published on {{> published datetime=this.published}}</small>
{{/if}}

{{> platform items=this.macos title="Mac"}}
{{> platform items=this.linux title="Linux"}}

{{/with}}

{{#with this.value.versions}}
## Versions

{{#each this}}
<details>
<summary>{{this.version}}</summary>
{{#if this.published}}
<small>Published on {{> published datetime=this.published}}</small>
{{/if}}

{{> platform items=this.macos title="Mac"}}
{{> platform items=this.linux title="Linux"}}

</details>
{{/each}}
{{/with}}

{{/with}}

[UWE]: https://uwe.app/ "Universal Web Editor"
