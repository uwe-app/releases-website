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

## Versions

{{#with result.[0]}}
{{#each this.value.versions}}
<details>
<summary>{{@key}}</summary>
{{>platform items=this.macos title="Mac"}}
{{>platform items=this.linux title="Linux"}}
</details>

{{/each}}
{{/with}}

[UWE]: https://uwe.app/ "Universal Web Editor"
