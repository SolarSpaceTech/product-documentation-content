---
id: 32
title: Description of categoryDescription - Main Sections - Meta Properties
displayName: categoryDescription
order: 90
published: true
historyName: Description of meta property categoryDescription
historyDescription: The meta property categoryDescription provides a brief description of the article in the section on the main page to improve navigation.
---

# Property categoryDescription

**Meta property:** `categoryDescription`

**Data type:** String

**Scope of influence:**
![Property Influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/category-description.png)

<br/>

## [Description](description)

The meta property `categoryDescription` is used to provide a brief description of the article in a specific section on the main page of the documentation site.
This description is displayed along with the article title (`categoryName`) and helps users quickly understand the content and value of the article.
The `categoryDescription` property plays an important role in attracting users' attention and improving their interaction with the documentation.

<br/>

### [Main Functions](basic-functions)

- **Providing a brief description:** Allows you to add a short text describing the main idea or content of the article, helping users understand what to expect from the article.
- **Improving user experience:** Helps users find the necessary information faster, making site navigation more intuitive and convenient.

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **`category`:** Defines the section on the main page where the article will be displayed. `categoryDescription` is applied to articles within this section.
- **`categoryName`:** The name of the article in the section on the main page. `categoryDescription` is displayed next to `categoryName`, providing additional information.
- **`categoryOrder`:** Determines the display order of the article within the section. Does not affect `categoryDescription`, but together they form a complete representation of the article in the section.
- **`categoryIcon`:** An icon displayed next to the article title. In combination with `categoryDescription`, it makes the representation of the article more intuitive.
- **`published`:** Determines the visibility of the article on the main page and other interface elements.

<br/>

### [Important Notes](notes)

- **Mandatory:** `categoryDescription` is not a mandatory property. However, its use is recommended to enhance the perception of the article on the main page.
- **Text Length:** It is recommended to be concise - usually up to 25 characters, so the description is fully displayed and easily readable.

<br/>

### [When to Use](when-to-use)

- **To Attract Attention:** To engage users and encourage them to read the article.
- **To Clarify Content:** When the article title (`categoryName`) may not be informative enough on its own.

<br/>

### [Usage Tips](advice)

- **Adapt to the Audience:** Consider the level of preparation and interests of your target audience when composing the description.
- **Be Specific:** The description should accurately reflect the content of the article and the benefit the user will receive.

<br/>

## [Conclusion](conclusion)

The `categoryDescription` meta property is an important tool for improving the presentation of articles in sections on the main documentation page. It helps users quickly understand what each article offers and make a decision about reading it.

<br/>

## [Usage Examples](examples)

### Example 1: Article in the `start` section

```md
---
title: Quick Start with Our Product
displayName: Quick Start
order: 1
published: true
category: start
categoryName: Getting Started
categoryDescription: Start using the product in minutes
categoryOrder: 10
categoryIcon: /icons/quickstart.svg
---

# Quick Start with Our Product

Welcome! In this guide, we will show you how to quickly set up and start working with our product...
```

**`categoryDescription`:** "Start using the product in minutes" provides a brief and attention-grabbing description of the article.

<br/>

### Example 2: Article in the `faq` section

```md
---
title: Frequently Asked Questions
displayName: FAQ
order: 5
published: true
category: faq
categoryName: Questions and Answers
categoryDescription: Answers to frequently asked questions by users
categoryOrder: 20
categoryIcon: /icons/faq.svg
---

# Frequently Asked Questions

In this section, you will find answers to the most popular questions...
```

**`categoryDescription`:** "Frequently Asked Questions" helps users understand what they will find in the article.
