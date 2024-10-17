---
id: 38
title: Description of footerName - Footer - Meta properties
displayName: footerName
order: 140
published: true
historyName: Description of the meta property footerName
historyDescription: The meta property footerName sets the name of the link to the article displayed in the footer of the documentation for quick access to important sections.
---

# Property footerName

**Meta property:** `footerName`

**Data type:** String

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/footer-name.png)

<br/>

## [Description](description)

The meta property `footerName` is used to set the name of the link to the article in the documentation footer. The footer is an important element
of the documentation interface that provides quick access to the most important or frequently used sections and articles.
By using `footerName`, you can select specific articles to display in the footer and set appropriate names for them.

<br/>

### [Basic Functions](basic-functions)

- **Display in documentation footer:** The value of `footerName` is used as the text of the link to the article displayed in the documentation footer.
- **Quick access:** Allows users to quickly navigate to key sections or articles from any point in the documentation.
- **Footer customization:** Provides the ability to customize the set of links in the footer to match the documentation needs and priorities.

<br/>

### [How it works with other meta properties](with-other-properties)

- **With `footerOrder`:** Determines the order of displaying the link in the footer. Articles with a lower `footerOrder` value are displayed to the right
  or below (depending on the documentation design).
- **With `published`:** If `published` is set to `false`, the article will not be displayed in the footer, even if `footerName` and `footerOrder` are specified.
- **With `displayName` and `title`:** `footerName` may differ from `displayName` and `title`, allowing you to set an alternative name for the article specifically for the footer.
- **With other meta properties:** Does not affect the display of the article in the menu, header, or other interface elements.

<br/>

### [Important Notes](notes)

- **Mandatory:** To display the article in the footer, both `footerName` and `footerOrder` must be specified. If one of them is missing, the link in the footer will not appear.
- **Uniqueness:** It is recommended that the names of the links in the footer are unique to avoid confusion.
- **Name Length:** Try to use short and clear names to ensure they are displayed correctly in the footer and do not disrupt the documentation design.

<br/>

### [When to Use](when-to-use)

- **Highlighting Key Sections:** To provide quick access to the most important or frequently used sections of the documentation.
- **Improving Navigation:** When it is necessary to make it easier for users to navigate to specific sections from any part of the documentation.

<br/>

### [Usage Tips](advice)

- **Conciseness and Clarity:** Use short names that are easily understood by users.
- **Content Relevance:** Ensure that `footerName` accurately reflects the content of the article.
- **Display Testing:** Test how the names appear in the footer on different devices and screens.
- **Optimal Number of Links:** Do not overload the footer with a large number of links. It is recommended to place no more than 5-7 links to maintain a clean design.
- **Priority:** Use `footerOrder` to prioritize links based on importance.
- **Consistent Style:** Maintain a consistent style of names in the footer.

<br/>

## [Conclusion](conclusion)

The `footerName` meta property is an important tool for customizing the documentation footer, allowing you to highlight key sections and improve navigation throughout the documentation. Proper use of `footerName` enhances the usability of the documentation and provides users with quick access to the most important information.

---

## [Usage Examples](examples)

### Example 1: Adding an Article to the Footer

```md
---
title: Getting Started with Documentation
displayName: Introduction
order: 1
published: true
footerName: Getting Started
footerOrder: 10
---

# Getting Started with Documentation

Welcome to the guide on getting started with our documentation...
```

- **`footerName`:** "Home" will be displayed in the footer of the documentation as the name of the link to this article.
- **`footerOrder`:** The value `10` determines the position of the link in the footer relative to other links.

<br/>

### Example 2: Article without displaying in the footer

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

**Result:** Since `footerName` and `footerOrder` are not specified, the article will not be displayed in the footer of the documentation.
