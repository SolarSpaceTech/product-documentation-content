---
id: 18
title: Headings - Markdown Markup
displayName: Headings
order: 10
published: true
historyName: Headings
historyDescription: Usage in Markdown Markup
---

# Headings

This section covers headings and how to use them.

<br/>

## [Description](description)

There are 6 levels of headings:

| MD Markup | Converts to HTML | Description     |
| :-------- | :--------------- | :-------------- |
| #         | h1               | Heading 1 level |
| ##        | h2               | Heading 2 level |
| ###       | h3               | Heading 3 level |
| ####      | h4               | Heading 4 level |
| #####     | h5               | Heading 5 level |
| ######    | h6               | Heading 6 level |

<br/>

## [Headings in Table of Contents](heading-in-table-of-contents)

To create a heading that will be added to the table of contents, you need to add a link within the heading. If there is other markup present along with the link, it will not be considered.

The structure for creating a linked heading:

```md
# [Content displayed in heading](link-to-heading "Title in Table of Contents")
```

- `Content displayed in heading` will be visible as the heading after content generation;
- `link-to-heading` will be used for navigation and will also change the hash in the URL when scrolling to the heading;
- `Title in Table of Contents` - optional. Used in the table of contents to display a title different from the content heading. If omitted, the table of contents will display `Content displayed in heading`.

<br/>

## [Usage](using)

There can only be 1 heading of level 1 on the page, otherwise the page's table of contents will be incorrectly generated.
If a heading should not be displayed in the table of contents, instead of:

```
# [Content displayed in heading](link-to-heading "Title in Table of Contents")
```

you can use:

```
# Content displayed in heading
```

The heading can be of any level.

<br/>

## Usage Example

```
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
```

<br/>

## Result

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6
