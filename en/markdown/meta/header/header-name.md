---
id: 40
title: Description of headerName - Header - Meta properties
displayName: headerName
order: 120
published: true
historyName: Description of the meta property headerName
historyDescription: The meta property headerName sets the title of the link to the article displayed in the documentation header for quick access to important sections.
---

# Property headerName

**Meta property:** `headerName`

**Data type:** String

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/header-name.png)

<br/>

## [Description](description)

The meta property `headerName` is used to set the title of the link to the article in the documentation header. The header is an important element of the documentation interface that provides quick access to the most important or frequently used sections and articles.
By using `headerName`, you can select specific articles to display in the header and set appropriate titles for them.

<br/>

### [Basic Functions](basic-functions)

- **Display in documentation header:** The value of `headerName` is used as the text of the link to the article displayed in the documentation header.
- **Quick access:** Allows users to quickly navigate to key sections or articles from any point in the documentation.
- **Header customization:** Provides the ability to customize the set of links in the header to match the documentation's needs and priorities.

<br/>

### [How it works with other meta properties](with-other-properties)

- **With `headerOrder`:** Determines the order in which the link is displayed in the header. Articles with a lower `headerOrder` value are displayed to the left or above (depending on the screen resolution).
- **With `published`:** If `published` is set to `false`, the article will not be displayed in the header, even if `headerName` and `headerOrder` are specified.
- **With `displayName` and `title`:** `headerName` may differ from `displayName` and `title`, allowing you to set an alternative title for the article specifically for the header.
- **With other meta properties:** Does not affect the display of the article in the menu, footer, or other interface elements.

<br/>

### [Important Notes](notes)

- **Mandatory:** To display an article in the header, both `headerName` and `headerOrder` must be specified. If one of them is missing, the link will not appear in the header.
- **Uniqueness:** It is recommended that the names of the links in the header are unique to avoid confusion.
- **Name Length:** Try to use short and clear names so that they are correctly displayed in the header and do not disrupt the documentation design.

<br/>

### [When to Use](when-to-use)

- **Highlighting Key Sections:** To provide quick access to the most important or frequently used sections of the documentation.
- **Improving Navigation:** When it is necessary to make it easier for users to navigate to specific sections from any part of the documentation.

<br/>

### [Usage Tips](advice)

- **Conciseness and Clarity:** Use short names that are easily understood by users.
- **Content Relevance:** Ensure that `headerName` accurately reflects the content of the article.
- **Display Testing:** Test how the names appear in the header on different devices and screens.
- **Optimal Number of Links:** Do not overload the header with a large number of links. It is recommended to place no more than 5 links to maintain a clean design.
- **Priority:** Use `headerOrder` to prioritize links based on importance.
- **Consistent Style:** Maintain a consistent style for header names.

<br/>

## [Conclusion](conclusion)

The `headerName` meta property is an important tool for customizing the documentation header, allowing you to highlight key sections and improve navigation through the documentation.
Proper use of `headerName` enhances the usability of the documentation and provides users with quick access to the most important information.

<br/>

## [Usage Examples](examples)

### Example 1: Adding an Article to the Header

```md
---
title: Getting Started with Documentation
displayName: Introduction
order: 1
published: true
headerName: Getting Started
headerOrder: 10
---

# Getting Started with Documentation

Welcome to the guide on getting started with our documentation...
```

- **`headerName`:** "Start" will be displayed in the documentation header as a link to this article.
- **`headerOrder`:** The value `10` determines the position of the link in the header relative to other links.

<br/>

### Example 2: Article without display in the header

```md
---
title: Detailed Technical Information
displayName: Technical Details
order: 5
published: true
---

# Detailed Technical Information

In this section, we will examine technical aspects in detail...
```

**Result:** Since `headerName` and `headerOrder` are not specified, the article will not be displayed in the documentation header.
