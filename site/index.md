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
