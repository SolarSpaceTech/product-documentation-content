---
id: 35
title: Description of categoryOrder - Main Sections - Meta Properties
displayName: categoryOrder
order: 100
published: true
historyName: Description of the meta property categoryOrder
historyDescription: The meta property categoryOrder sets the order of displaying articles within a section on the main page for easy navigation.
---

# Property categoryOrder

**Meta property:** `categoryOrder`

**Data type:** Number

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-order.png)

<br/>

## [Description](description)

The meta property `categoryOrder` is used to determine the order of displaying an article within a specific section on the main page of the website.
It allows you to precisely configure the sequence of articles in the section, providing control over which article will be shown first, second, and so on.

<br/>

### [Basic Functions](basic-functions)

- **Managing the order of articles in a section:** Allows you to arrange articles in the desired sequence within a single section on the main page.
- **Display priority:** Articles with a lower `categoryOrder` value are displayed higher in the section list, giving them a higher priority.

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **`category`:** Defines the section on the main page where the article will be displayed. `categoryOrder` is only applied to articles within the same section.
- **`categoryName`:** Sets the name of the article displayed in the section on the main page.
- **`categoryDescription`:** Provides a brief description of the article to be displayed in the section.
- **`categoryIcon`:** Specifies the path to the icon displayed next to the article name in the section.

<br/>

### [Important Notes](notes)

- **Mandatory:** `categoryOrder` is mandatory if it is decided to specify an article in one of the sections.
- **Uniqueness of values:** It is recommended to use unique values for `categoryOrder` within a single section for precise control of the display order.
- **Value range:** Can take any integer values. Positive numbers are usually used for ease of management.


<br/>

### [When to Use](when-to-use)

- **Sequence Control:** When it is important for articles to be displayed in a specific order, for example, from introductory materials to more complex ones.
- **Setting Priorities:** To highlight more important or current articles by placing them higher in the section.
- **Content Organization:** For logical grouping and sequence of presenting information to users.

<br/>

### [Usage Tips](advice)

- **Planning:** Plan the section structure and article distribution in advance to determine suitable `categoryOrder` values.
- **Grouping:** If the section has subcategories, you can use value ranges for each group (for example, 10-19 for one group, 20-29 for another).
- **Updating:** When adding new articles, try to maintain a logical sequence of `categoryOrder` values.
- **Incremental Steps:** Use steps between values (for example, 10, 20, 30) to make it easier to insert new articles between existing ones without the need to reassign all values.
- **Checking Uniqueness:** Ensure that `categoryOrder` values are unique within the section to avoid ambiguity in the display order.
- **Deliberate Order:** Plan the order of articles according to their importance and reading sequence.

<br/>

## [Conclusion](conclusion)

The `categoryOrder` meta property is a key tool for precise control of the display order of articles in sections on the main page.
It allows you to create a structured and logical interface, improving navigation and overall user experience on the site. Proper use
of this property contributes to effective content organization and enhances the usability of the resource.

<br/>

## [Usage Example](examples)

```md
---
title: Quick Start
displayName: Getting Started
order: 1
published: true
category: start
categoryName: Quick Start
categoryDescription: Learn how to quickly get started with our service
categoryOrder: 10
categoryIcon: /icons/quickstart.svg
---

# Quick Start

Welcome to the quick start guide...
```

```md
---
title: Deep Dive
displayName: Advanced Usage
order: 2
published: true
category: start
categoryName: Deep Dive
categoryDescription: Detailed guide for experienced users
categoryOrder: 20
categoryIcon: /icons/deepdive.svg
---

# Deep Dive

In this guide, we will take a detailed look at...
```
