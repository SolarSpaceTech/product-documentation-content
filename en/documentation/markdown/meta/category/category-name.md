---
id: 34
title: Description of categoryName - Main Sections - Meta Properties
displayName: categoryName
order: 80
published: true
historyName: Description of the meta property categoryName
historyDescription: The meta property categoryName sets the title of the article to be displayed in a section on the main page, improving navigation.
---

# Property categoryName

**Meta property:** `categoryName`

**Data type:** String

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-name.png)


<br/>

## [Description](description)

The meta property `categoryName` is used to define the title of the article displayed in a specific section on the main page of the site.
This title will be shown to users in the corresponding section (`start`, `services`, `useful`, or `faq` determined by the `category` property)
when they are viewing the main page.

<br/>

### [Basic Functions](basic-functions)

- **Setting a title for the main page:** Allows you to specify a specific title for the article that will be displayed only in the section
on the main page, different from the main title of the article (`displayName`).

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **`category`:** Determines in which section of the main page the article will be displayed.
Takes one of the values: `start`, `services`, `useful`, `faq`.
- **`categoryDescription`:** Provides a brief description of the article to be displayed in the section on the main page.
- **`categoryOrder`:** Determines the order of displaying the article within the section on the main page.
- **`categoryIcon`:** Specifies the path to the icon displayed next to the article title in the section.
- **`displayName`:** The general title of the article used in the menu and breadcrumbs. `categoryName` and `displayName` may differ.

<br/>

### [Important Notes](notes)

- **Mandatory:** To display the article in a section on the main page, both `category` and `categoryName` must be specified.
- **Absence of `categoryName`:** If `category` is specified but `categoryName` is missing, the value from `displayName` will be used for display.
- **Uniqueness of the title:** It is recommended that `categoryName` be informative and unique within the section to avoid confusion.


<br/>

### [When to Use](when-to-use)

- **Adapting the title for the main page:** When it is necessary to present an article with a more suitable title for the main page.
- **Differences in titles:** If the article title in the menu or header is too long or technical for the main page.

<br/>

### [Usage Tips](advice)

- **Consistency:** Ensure that `categoryName` aligns with the content of the article and does not mislead users.
- **Testing:** Check how `categoryName` looks on the main page alongside `categoryDescription` and the icon.

<br/>

## [Conclusion](conclusion)

The `categoryName` meta property is an important tool for customizing the display of articles on the main page. It allows content to be presented
most effectively and attractively to users visiting the documentation.

<br/>

## [Usage Example](examples)

```md
---
title: Complete Setup Guide
displayName: Setup Guide
order: 5
published: true
category: services
categoryName: Quick Setup
categoryDescription: Learn how to quickly set up our service
categoryOrder: 1
categoryIcon: /icons/setup.svg
---
# Complete Setup Guide

Welcome to the complete setup guide for our service...
```

In this example:
- **`category`:** The article will be displayed in the `services` section on the main page.
- **`categoryName`:** In the `services` section, the article will be displayed under the name "Quick Setup".
- **`categoryDescription`:** A brief description "Learn how to quickly set up our service" will be displayed under the name.
- **`categoryOrder`:** The article will be the first in the `services` section list.
- **`categoryIcon`:** An icon `/icons/setup.svg` will be displayed next to the article name.
