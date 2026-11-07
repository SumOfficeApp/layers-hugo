# Layers shortcodes for Hugo

**Your Hugo site readers open, fill in and sign .docx and .xlsx files in one click.**

Two shortcodes for Hugo sites. A link to a `.docx`, `.xlsx` or `.pptx` file gets a button: your reader opens the file, fills it in and sends it for signature in the browser. A live document from the Layers catalog sits right on the page.

## Install

```bash
hugo mod init github.com/you/your-site   # once, if your site is not a module yet
```

`hugo.toml`:

```toml
[module]
  [[module.imports]]
    path = "github.com/SumOfficeApp/layers-hugo"
```

## Use

```markdown
{{</* layers-doc src="/files/service-agreement.docx" title="Service agreement" */>}}

{{</* layers-form slug="freelance-invoice-payment-reminder" height="720" */>}}
```

| Shortcode | Parameters |
|---|---|
| `layers-doc` | `src` (file, local or a link), `title`, `label`, `from` |
| `layers-form` | `slug` from the catalog, `height`, `title`, `from` |

The file must be reachable by a public link once your site is live. Nothing goes to Layers until the reader clicks.

See it working on a real contract: https://sumofficeapp.github.io/layers-embed/

## What your reader gets

The document opens in Layers as a fast page, on a phone too: edit it, send it for signature, save a finished copy. Start free: https://app.layers.md/register?from=door-hugo. Plans: https://layers.md/pricing?from=door-hugo.

MIT. Made by SumOffice.
