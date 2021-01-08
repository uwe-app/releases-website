+++
title = "Home"
+++

Thanks for choosing [UWE][] and welcome to your new website!

You can find a lot of information in the [documentation][docs] and if you have questions reach out in the [community discussions][]. If you encounter a bug please report it in the [community issues][].

## Content

Edit the `site/index.md` file to change the content of *this page*; to create new pages add markdown files with a `.md` extension to the `site` folder.

Edit the `site/partials/header.hbs` and `site/partials/footer.hbs` files to change the website header and footer.

> Note that adding files and editing partials currently requires a restart when live reload is enabled.

## Styles

Included are some basic styles but you probably want to use your own; edit the `site/assets/styles/main.css` file to customize the styles for this website.

To remove the included stylesheet delete this line from `site.toml`:

```toml
apply = { styles = ["**"] }
```

Learn more in the [styles documentation][styles].

## Scripts

To add a script to all your pages create the `site/assets/scripts/main.js` file.

Learn more in the [scripts documentation][scripts].

## Links

To create links to other pages use wiki syntax, for example, if you have a `site/contact.md` file with some content you can link to it like this:

```text
\[[contact]]
```

Learn more in the [links documentation][links].

## Syntax Highlighting

To enable syntax highlighting for your project add these settings to `site.toml`:

```toml
[syntax]
inline = true
theme = "Solarized (light)"
```

More information and a list of available themes is in the [syntax highlighting guide][syntax].

## Build Tools

To integrate with a Javascript bundler or CSS pre-processor see the [integrations guide][integrations].

---

<details>
<summary>Template data for this page</summary>
<pre>{{{json this pretty=true}}}</pre>
</details>

[UWE]: https://uwe.app/ "Universal Web Editor"
[docs]: https://uwe.app/docs/ "UWE Documentation"
[integrations]: https://uwe.app/docs/getting-started/integrations/ "Integrations Documentation"
[styles]: https://uwe.app/docs/getting-started/styles/ "Styles Documentation"
[scripts]: https://uwe.app/docs/getting-started/scripts/ "Scripts Documentation"
[links]: https://uwe.app/docs/getting-started/links/ "Links Documentation"
[syntax]: https://uwe.app/docs/content/syntax-highlight/ "Syntax Highlight Documentation"
[community discussions]: https://github.com/uwe-app/community/discussions "Community Discussions"
[community issues]: https://github.com/uwe-app/community/issues "Community Issues"
