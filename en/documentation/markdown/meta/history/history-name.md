---
id: 43
title: Description of historyName - History - Meta properties
displayName: historyName
order: 50
published: true
historyName: Description of the meta property historyName
historyDescription: The meta-property historyName sets the title of the article in the visit history block, improving navigation and returning to articles.
---

# Property historyName

**Meta property:** `historyName`

**Data type:** String

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/history-name.png)

<br/>

## [Description](description)

The meta property `historyName` is used to set the title of the link to the article in the visit history block in the documentation. This block displays the last articles visited by the user, providing quick access to previously viewed material. `historyName` helps users easily identify articles by clear and informative names in the history.

<br/>

### [Basic Functions](basic-functions)

- **Displaying the title in the visit history:** The value of `historyName` is displayed in the visit history block as the title of the article link.
- **Improving navigation:** Helps users quickly find and return to previously viewed articles.
- **Personalizing the experience:** Allows you to customize the displayed article title in the history independently of its main name in the menu or header.

<br/>

### [How it works with other meta properties](with-other-properties)

- **With `historyDescription`:** Provides a brief description of the article in the visit history block, complementing `historyName`.
- **With `title` and `displayName`:** `historyName` may differ from `title` and `displayName`, allowing you to set an alternative title for the visit history.

<br/>

### [Important Notes](notes)

- **Mandatory:** The meta property `historyName` is not mandatory. If not specified, the value of `displayName` or `title` may be used in the visit history block.
- **Uniqueness:** It is recommended that `historyName` be informative and reflect the content of the article, but uniqueness is not mandatory.
- **Language and style:** Use clear and context-appropriate names to facilitate users in recognizing the article in the history.


<br/>

### [When to Use](when-to-use)

- **For customizing the name:** When you want the article title in the visit history to be different from `displayName` or `title`.
- **For providing context:** If `displayName` is too short or does not fully reflect the content, `historyName` can provide a more informative title.

<br/>

### [Usage Tips](advice)

- **Personalizing the title:** Use `historyName` to provide users with the most relevant and understandable article title in the visit history.
- **Optimizing for mobile devices:** Consider the limited screen space on mobile devices and avoid overly long titles.
- **Display testing:** Check how `historyName` looks in the visit history block to ensure correct display.
- **Consistency:** Ensure that `historyName` aligns with the content of the article and does not mislead users.
- **Conciseness:** Aim for short and clear titles that display well in the interface.
- **Relevance:** Update `historyName` if the content of the article has significantly changed.

<br/>

## [Conclusion](conclusion)

The `historyName` meta property is a useful tool for improving navigation in documentation, allowing customization of displayed article names in the visit history block. This contributes to a more convenient and personalized user experience, making it easier for them to return to previously viewed materials. Proper use of `historyName` enhances the efficiency of interacting with documentation and improves the overall impression of using the site.

<br/>

## [Usage Examples](examples)

### Example 1: Article with a custom name in the visit history

```md
---
title: Installation Guide
displayName: Installation
order: 1
published: true
historyName: Quick Start - Installation
historyDescription: How to quickly install and configure the product
---
# Installation Guide

In this section, you will learn how to install our software...
```

- **`historyName`:** "Quick Start - Installation" is displayed in the visit history block.
- **`historyDescription`:** Provides a brief description for additional context.

### Example 2: Using `historyName` matching `displayName`

```md
---
title: Frequently Asked Questions
displayName: FAQ
order: 10
published: true
historyName: FAQ
historyDescription: Answers to the most common questions
---
# Frequently Asked Questions

Here you will find answers to frequently asked questions...
```

- **`historyName`:** "FAQ" is displayed in the visit history, matching `displayName`.
```
