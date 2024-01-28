# hexo-fontawesome-icons

![NPM Downloads](https://img.shields.io/npm/dm/hexo-fontawesome-icons)

<a href="https://www.npmjs.com/package/hexo-fontawesome-icons"><img alt="" src="https://img.shields.io/npm/dm/hexo-fontawesome-icons
"></a>

A plugin for static pages generator [Hexo](https://github.com/hexojs/hexo).
A utility function which helps to inline fontawesome SVG files.

## Installation

### Requirements

- NodeJS at least 6.x

### CLI

Install this plugin and all free font-awesome styles:

```bash
npm install hexo-fontawesome-icons --save
```

## Usage

### In theme

This plugin adds a view helpers you can use in the theme to include inline SVG icons
from the font-awesome collection.

#### fa_css()

Returns inline styles needed for the inline SVGs.

Example usage:

```html
<style>
  <%- fa_css() %>
</style>
```

in EJS template or

```html
<style>
  {{ fa_css() }}
</style>
```

in NunJucks tempalte

#### fa_inline(iconName, options)

Returns an SVG markup of the chosen icon.

Possible options:

- `prefix` - the style prefix, `fab` for brands, `fas` for solid etc. Defaults to `fas`

```ejs
<%- fa_inline('twitter', { prefix: 'fab' }) %>  // in EJS template
```

```njk
{{ fa_inline('twitter', { prefix: 'fab' }) }}  // in NunJucks template
```

### In post

This plugin adds a tag that you can use in the theme to include inline SVG icons
from the font-awesome collection.

#### {% fa_css %}

Returns inline styles needed for the inline SVGs.

Example usage:

```md
# My
## Post
### Content
#### Here

{% fa_css %}
```

#### {% fa_inline iconName [prefix] %}

Returns an SVG markup of the chosen icon.
`prefix` is the style prefix, `fab` for brands, `fas` for solid etc. Defaults to `fas`

Example usage:

```md
# My
## Post
### Content
{% fa_inline twitter fab %}
#### Here

{% fa_css %}
```

## Acknowledgments

Special thanks to [hexojs](https://github.com/hexojs) for creating the original [hexo-fontawesome](https://github.com/hexojs/hexo-fontawesome) on which this project is based.
