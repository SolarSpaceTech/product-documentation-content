---
id: 47
title: Description title - General - Meta properties
displayName: title
order: 20
published: true
historyName: Description meta property title
historyDescription: The meta property title displays the page title on the browser tab, making navigation and section identification easier.
---

# Property title

**Meta property:** `title`

**Data type:** String

<br/>

## [Description](description)

The meta property `title` is used to specify the text that will be displayed in the browser tab title when viewing the documentation page. 
This property is particularly important in the context of generating documentation, as it helps users quickly determine the content of the current page and facilitates
navigation between documentation sections.

<br/>

### [Main functions](basic-functions)

- **Display in browser tab:** The `title` value is displayed on the browser tab, helping users navigate the documentation,
especially when working with multiple open tabs.
- **Identification of documentation section:** Allows to clearly indicate the topic or section being discussed on the page.
- **Support for bookmarks and browser history:** When saving a page to bookmarks or viewing visit history, `title` is used as the page title,
making it easier to return to the desired documentation section.

<br/>

### [How it works with other meta properties](with-other-properties)

- **`displayName`:** Defines the article name in the menu and breadcrumbs. It can be shorter or more user-friendly, while `title` can contain a more detailed description.
- **`order`:** Specifies the display order of the article in the menu, but does not affect `title`.
- **`published`:** Determines whether the article will be accessible to users, but does not affect `title`.

<br/>

### [Important notes](notes)

- **Consistency:** It is recommended that `title` reflects the content of the page and is consistent with other meta properties, such as `displayName`.
- **Length:** The optimal length of `title` is up to 60 characters to be fully displayed on browser tabs and bookmarks.
- **Uniqueness:** Each documentation section should have a unique `title` to avoid confusion.


<br/>

### [When to Use](when-to-use)

- **Always when creating documentation articles:** This is a mandatory property for each page to ensure clarity and ease of use.
- **For content clarification:** When it is necessary to describe the content of the page in more detail than `displayName` allows.
- **For improved navigation:** Helps users quickly navigate through the numerous sections of the documentation.

<br/>

### [Usage Tips](advice)

- **Be specific:** Reflect the exact content of the page in the `title` so that users immediately understand what is being discussed.
- **Avoid excessive length:** Strive to make the title informative but not too long.
- **Use separators:** If necessary, separate parts of the title with a colon or dash to improve readability.
- **Reflect the documentation structure:** If an article is part of a larger section, you can indicate this in the `title` (e.g., "Setting up Environment - Developer's Guide").
- **Consider the audience:** Use clear and commonly accepted terms appropriate to the readers' level of expertise.
- **Avoid duplication:** A unique `title` for each page will help users and search engines distinguish sections from each other.

<br/>

## [Conclusion](conclusion)

The `title` meta property is an important element in generating documentation. It helps users quickly understand the information contained on the current page and facilitates navigation through the documentation sections. A properly formulated `title` enhances usability and contributes to more effective learning of the materials.

<br/>

## [Usage Examples](examples)

### Example 1: Article on Software Installation

```md
---
title: Software Installation - Getting Started Guide
displayName: Software Installation
order: 1
published: true
---
# Software Installation

In this section, you will learn how to install our software on your system...
```

- **`title`:** "Software Installation - Getting Started Guide" will be displayed on the browser tab.
- **`displayName`:** "Software Installation" will be shown in the menu and breadcrumbs, providing brevity and ease of navigation.


<br/>

### Example 2: Article about API Documentation

```md
---
title: API Documentation — Methods and Endpoints
displayName: API Documentation
order: 5
published: true
---
# API Documentation

This section contains a detailed description of available API methods and endpoints...
```

- **`title`:** "API Documentation — Methods and Endpoints" clearly indicates the content of the page.
- **`displayName`:** "API Documentation" is used for navigation.
```
