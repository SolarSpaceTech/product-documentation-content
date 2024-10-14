---
id: 42
title: Description of historyDescription - History - Meta property
displayName: historyDescription
order: 60
published: true
historyName: Description of the historyDescription meta property
historyDescription: The historyDescription meta property provides a brief description of the article in the browsing history, improving navigation and reminding of the content.
---

# Property historyDescription

**Meta property:** `historyDescription`

**Data type:** String

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/history-description.png)

<br/>

## [Description](description)

The `historyDescription` meta property is used to provide a brief description of the article in the browsing history block. This block displays articles recently viewed by the user, providing quick access to previously read content. `historyDescription` complements `historyName`, providing additional context and helping users recall the content of the article.

<br/>

### [Basic Functions](basic-functions)

- **Displaying description in browsing history:** The value of `historyDescription` is displayed along with `historyName` in the browsing history block, providing a brief summary of the article's content.
- **Improving navigation:** Helps users find the necessary information faster, reminding them of the content of previously viewed articles.
- **Personalizing the experience:** Allows customization of the displayed article description in the history independently of the main article content.

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **With `historyName`:** `historyDescription` complements `historyName`, providing more complete information about the article in the browsing history block.
- **With `title` and `displayName`:** While `title` and `displayName` define the names of the article in other parts of the interface, `historyDescription` provides a specific description for the browsing history.

<br/>

### [Important Notes](notes)

- **Mandatory:** The `historyDescription` meta property is not mandatory. If not specified, only `historyName` may be displayed in the browsing history block without a description.
- **Length:** It is recommended to be concise, usually up to 150 characters, to fully display the description in the interface without truncation.
- **Language and Style:** Use clear and simple language to effectively convey the essence of the article.


<br/>

### [When to Use](when-to-use)

- **To provide context:** When the article title is not informative enough, `historyDescription` helps users remember what the article was about.
- **To attract attention:** A brief and concise description can encourage users to return to the article.
- **To enhance user experience:** Providing additional information in the visit history makes navigation more convenient.

<br/>

### [Usage Tips](advice)

- **Content relevance:** Make sure the description accurately reflects the content of the article.
- **Be concise and informative:** Try to convey the main idea of the article in one or two sentences.
- **Check the display:** Ensure that `historyDescription` is correctly displayed in the interface and is not truncated.

<br/>

## [Conclusion](conclusion)

The `historyDescription` meta property is a useful tool for improving documentation navigation. By providing a brief and informative description of articles in the visit history block, you make it easier for users to return to the necessary material and increase the efficiency of using your documentation.

<br/>

## [Usage Examples](examples)

### Example 1: Article with a Custom Description in Visit History

```md
---
title: Installation Guide
displayName: Installation
order: 1
published: true
historyName: Quick Start - Installation
historyDescription: Learn how to install our product in a few steps
---
# Installation Guide

In this section, you will learn how to install our software...
```

- **`historyDescription`:** "Learn how to install our product in a few steps" is displayed in the visit history block, providing a brief description of the article.

<br/>

### Example 2: Article without `historyDescription` Specified

```md
---
title: Frequently Asked Questions
displayName: FAQ
order: 10
published: true
historyName: FAQ
---
# Frequently Asked Questions

Here you will find answers to frequently asked questions...
```

- **Result:** Only `historyName` will be displayed in the visit history block without a description.

Please provide me with the Markdown document you need to be translated from Russian to English.
