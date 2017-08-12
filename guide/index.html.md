---
layout: plugin-documentation.html.ejs
title: AskashaCMS Breadcrumbs plugin documentation
---
The breadcrumb trail at the top of each page on this site is generated by `akashacms-breadcrumbs`.  Generally speaking, an AkashaCMS breadcrumb trail is a sequence of links to pages from the webroot down to the current document.  This allows the reader to easily navigate to any page in the hierarchy.

# Installation

Add the following to `package.json`

```
"dependencies": {
      ...
      "akashacms-breadcrumbs": ">=0.6",
      ...
}
```


Once added to `package.json` run: `npm install`

# Configuration

Add the following to `config.js`

```
config
    ...
    .use(require('akashacms-breadcrumbs'))
    ...
```

# Custom Tags

#### Generating the breadcrumb trail

Use this tag: `<breadcrumb-trail/>`

The code uses the `breadcrumbTrail` function, internal to the plugin, to search upward from the current document.  It locates each page named `index.html` and extracts its title, generating a link to each one.