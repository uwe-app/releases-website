+++
title = "Software Releases"
+++

# {{title}}

Software releases for the [UWE][] platform tools; to install the latest release run:

```
curl https://releases.uwe.app/install.sh | sh
```

To update to the latest version run:

```
uvm update
```

{{#with result.[0]}}
{{#with this.value.latest}}

## Latest {{this.version}}

{{>platform items=this.macos title="Mac"}}
{{>platform items=this.linux title="Linux"}}

{{/with}}

## Versions

{{#each this.value.versions}}
<details>
<summary>{{this.version}}</summary>
{{>platform items=this.macos title="Mac"}}
{{>platform items=this.linux title="Linux"}}
</details>
{{/each}}

{{/with}}

[UWE]: https://uwe.app/ "Universal Web Editor"
