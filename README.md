# CTM website

Portal with a directory of legal resources and community contacts.

## Updating content

The homepages can be edited by opening the language-specific `index.md` files in `_homepage`.
- To make immediate changes, click the `Edit this file` button. 
- Content is written in Markdown. [Here's a 2-page PDF that contains syntax examples](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf). 

To add more pages, create a Markdown file named `_pages/en/my-new-page`. Add this to it:

```markdown
---
lang-ref: my-new-page
title: <!-- sets the window title -->
description: <!-- overrides the site description used in search results -->
subhead: <!-- displays text below logos -->
---

Hello, world!
```

Ready to translate `my-new-page`? Create a file named `_pages/es/mi-nueva-pagina` and use the same `lang-ref`.

### Edit the banner

- Banner content is controlled by `_data/banner.yml`. Remove the file's content to hide it.
- Here's how it works:

```yaml
text:
  en: # Style your text with Markdown
  es: # Add translations
link: # Declare a link on this line to apply it to all languages
  en: # Or add language-specific links
``` 

### Add bottom navigation

1. Create a file named `_data/nav.yml` and paste the following:

```yaml
elements:
  - group: 
    en: Add navigation
    es: Agregar navegación
    items:
      - page:
          en: Link to a page
          es: Enlace a una página
          url: 
            en: my-new-page
            es: mi-nueva-pagina
      - page:
          en: Another link
          es: Otro enlace
          url:
            en: my-new-page
            es: mi-nueva-pagina
  - group:
    en: Another group
    es: Otro grupo
    items:
      - page:
          en: Use Markdown *styling*
          es: Utilice Markdown *estilo*
          url:
            en: my-new-page
            es: mi-nueva-pagina
```

2. Commit these changes. You have a nav!
