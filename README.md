# markdown

<img src="https://img.shields.io/badge/Donna-markdown-FF6347?style=for-the-badge" alt="Donna markdown"/>
<a href="https://nikolasskyl.github.io/markdown/">
  <img src="https://img.shields.io/badge/Docs-Read-2F81F7?style=for-the-badge" alt="Docs - Read"/>
</a>
<img src="https://img.shields.io/github/actions/workflow/status/NikolasSkyl/markdown/test.yml?branch=main&label=Test&style=for-the-badge" alt="Test status"/>

Markdown to HTML conversion for the [Donna](https://github.com/donna-lang/donna) programming language.

## Overview

`markdown` is a small Donna wrapper around the MD4C C Markdown parser.

It exposes one focused function: convert a Markdown document string into an HTML fragment.

## Installation

Add to your `donna.toml` as a dependency:

```toml
[dependencies]
markdown = { git = "https://github.com/NikolasSkyl/markdown", version = ">=0.1.0 and <1.0.0" }
```

Then import the module:

```donna
import markdown
```

## Quick start

```donna
import markdown

pub fn render_post() -> String:
  markdown.to_html("# Hello Donna\n\nThis is **Markdown**.")
```

Use it in an app:

```donna
import markdown

pub fn main() -> Nil:
  echo markdown.to_html("Hello *Donna*")
```

Run tests:

```sh
donna test
```

## API

For API Reference visit the generated docs [here](https://nikolasskyl.github.io/markdown/)

## Output

`to_html` returns an HTML fragment:

```donna
markdown.to_html("# Hello")
```

```html
<h1>Hello</h1>
```

## Credits

This package vendors [MD4C](https://github.com/mity/md4c), which is distributed under the MIT licence.

## Licence

MIT
