---
id: 1
title: Creating Articles - File Structure
displayName: Creating Articles
order: 20
published: true
historyName: Creating Articles
historyDescription: Guide to creating articles with metadata for generating the interface in the application.
---

# Creating Articles

In this article, we will briefly discuss the process of creating articles for documentation, from which HTML pages are generated based on the file structure
with `*.md` files and their metadata. You will be able to effectively organize content, manage the display of user interface elements,
and provide convenient navigation for users.

<br/>

## File Structure

Each article is represented by a file with the extension `.md`, located in the corresponding section directory. The file structure reflects
the hierarchy of sections and subsections of the documentation.

- **Root directory**: contains language directories (`ru`, `en`, etc.).
- **Language directory**: includes the `metadata.md` file with language metadata and main page settings.
- **Sections and Subsections**: organized as directories inside the language directory, each of which may contain its own `metadata.md`.
- **Articles**: `.md` files located inside the respective section directories.

<br/>

## Article Metadata

At the top of each article file, it is necessary to specify metadata in **YAML** format between three dashes `---`. This metadata affects
the display of the article in various interface elements.

### Example of article metadata

```markdown
---
id: 42
title: User Guide
displayName: Guide
order: 10
published: true
historyName: Guide in History
historyDescription: Brief description of the user guide
category: Getting Started
categoryName: Quick Start
categoryDescription: Learn how to get started quickly
categoryOrder: 1
categoryIcon: /icons/start.svg
headerName: Guide in Header
headerOrder: 20
footerName: Guide in Footer
footerOrder: 10
---
```

### Description of key metadata properties

- `id`: unique identifier of the article within the language.
- `title`: page title in the browser.
- `displayName`: article name in the menu.
- `order`: display order of the article in the section menu.
- `published`: determines whether the article will be displayed in the interface.
- `historyName` and `historyDescription`: used in the visit history block.
- `category` and related properties: determine the display of the article on the main page in a specific section.
- `headerName` and `headerOrder`: display the link to the article in the site header.
- `footerName` and `footerOrder`: display the link to the article in the site footer.

<br/>

## Article Content

After the metadata, the main content of the article should follow, written in Markdown markup. Here you can use various Markdown elements
to format text, such as headers, lists, images, tables, etc.

### Example Article Content

```markdown
# User Manual

Welcome to the documentation! In this guide, you will learn how to get started and use the basic functions.

## Getting Started

To begin, you need to create a language directory and describe the main page.

<!-- Further steps description... -->
```

<br/>

## Using Variables

In the article text, you can use variables that will be replaced with values from the JSON response `white-label`. This allows dynamically inserting
data and maintaining the content's relevance.

### Variable Syntax

- Use double curly braces: `{{ var }}`.
- Access to nested properties is supported: `{{ company.name }}`.

### Example of Use

```markdown
Welcome to the company website {{ company.name }}! Visit our website: {{ company.domain }}.

Our partner: {{ deep.company.name }} ({{ deep.company.domain }})
```

### After Processing:

```markdown
Welcome to the company website Company example! Visit our website: https://company-example-domain.ru.

Our partner: Deep company example (https://deep-company-example-domain.ru)
```

<br/>

## Links and Navigation

### Creating Links to Articles

- **Standard links**: use a relative path based on the file structure.

```markdown
[Learn more](/en/documentation/guide)
```

- **Short links using `id`**: allow referencing articles by their identifier.

```markdown
[User Manual]([42])
```

<br/>

## Conclusion

Creating articles with the correct structure and metadata ensures efficient organization of content and enhances user interaction
with the documentation.
