---
id: 31
title: Description of category - Main sections - Meta properties
displayName: category
order: 70
published: true
historyName: Description of the meta property category
historyDescription: The meta-property category defines the section on the main page where the article will be displayed, simplifying navigation.
---

# Property category

**Meta property:** `category`

**Data type:** String

**Possible values:** values from the list specified in the `categories` property description in `metadata.md`

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/category.png)

<br/>

## [Description](description)

The meta property `category` is used to define a section on the main page of the site where the article will be displayed. This property links the article
to one of the predefined categories, allowing to structure the content on the main page and provide users with quick access to the most
relevant materials.

<br/>

### [Basic functions](basic-functions)

- **Defining a section on the main page:** Allows to distribute articles to specific sections defined in the `categories`.
- **Managing display on the main page:** Only articles with the specified `category` property will be displayed in the corresponding section on the main page.
- **Content organization:** Helps in grouping articles by theme or purpose to improve navigation.

<br/>

### [How it works with other meta properties](with-other-properties)

- **`categories`**: Sets the names of sections on the main page. If not specified in the language section, `category` will not work.
- **`categoryName`**: Sets the name of the article displayed in the section on the main page. If not specified, `displayName` can be used.
- **`categoryDescription`**: Provides a brief description of the article in the section on the main page.
- **`categoryOrder`**: Determines the order of displaying the article within the section on the main page.
- **`categoryIcon`**: Specifies the path to the icon displayed next to the article name in the section.

<br/>

### [Important Notes](notes)

- **Mandatory for display in section:** To have an article appear in a specific section on the main page, it is necessary to specify the properties: `category`, `categoryName`, and `categoryOrder`. For complete display, it is also recommended to specify `categoryDescription`.
- **Limited values:** `category` only accepts predefined values in `categories`. Using other values will not result in the article being displayed in the section.
- **Absence of `category`:** If the property is not specified, the article will not be displayed in any section on the main page, but will remain accessible through the menu or direct link.

<br/>

### [When to Use](when-to-use)

- **Placing key articles on the main page:** If you want certain articles to be easily accessible from the main page.
- **Grouping content by topics:** To organize articles into thematic sections, facilitating navigation for users.
- **Increasing visibility of important materials:** To draw attention to specific articles by placing them in prominent sections on the main page.

<br/>

### [Usage Tips](advice)

- **Careful selection of section:** Ensure that the article aligns with the theme of the selected section to maintain the logic of the documentation structure.
- **Supplement with other meta properties:** Use together with `categoryName`, `categoryDescription`, and `categoryIcon` to display the article in the section.
- **Content uniqueness:** Avoid duplicating articles in one section with the same names or descriptions; one article cannot be displayed in multiple sections.

<br/>

## [Conclusion](conclusion)

The meta property `category` is key to managing the display of articles on the main page of the documentation. It allows for efficient organization of content by distributing articles into thematic sections. Proper use of this property enhances navigation and user experience, helping visitors quickly find the information they need.

<br/>

## [Usage Example](examples)

```md
---
title: How to Get Started with Our Service
displayName: Beginner's Guide
order: 1
published: true
category: Getting Started
categoryName: Quick Start
categoryDescription: Step-by-step guide to a successful start
categoryOrder: 1
categoryIcon: /icons/getting-started.svg
---

# How to Get Started with Our Service

Welcome! In this guide, we will explain how to quickly start using our service...
```

In this example:

- **`category`:** The value is set to `Getting Started`, so the article will appear in the "Getting Started" section on the main page.
- **`categoryName`:** The section will display the name "Quick Start".
- **`categoryDescription`:** A brief description "Step by step to a successful start" will appear below the name.
- **`categoryOrder`:** The article will be displayed first in the "start" section.
- **`categoryIcon`:** An icon located at `/icons/getting-started.svg` will be displayed next to the article name.
