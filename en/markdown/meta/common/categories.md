---
id: 30
title: Description of categories - General - Meta properties
displayName: categories
order: 60
published: true
historyName: Description of the meta property categories
historyDescription: The meta-property categories defines the names and order of sections on the main page.
---

# Property categories

**Meta property:** `categories`

**Data type:** List of strings

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/category.png)

<br/>

## [Description](description)

A meta property used in the language section. It represents a list of strings and defines sections on the main page for the given language.
These sections are used to group articles by themes or functional features, making it easier for users to navigate and find the necessary information.

<br/>

### [Basic functions](basic-functions)

- **Defining sections on the main page:** The `categories` array sets the names of sections that will be displayed on the main page in the specified order.
- **Managing the order of sections:** The order of elements in the `categories` array determines the order of displaying sections on the main page.
- **Linking to articles:** Articles can be linked to specific sections through the `category` property in their metadata, corresponding to one
  of the values in `categories`.

<br/>

### [How it works with other meta properties](with-other-properties)

- `category`: Allows selecting the section in which the article will be displayed.
- `categoryName`: Allows setting a custom name for the article in the section.
- `categoryDescription`: Brief description of the article to be displayed in the section.
- `categoryOrder`: Determines the order of the article within the section.
- `categoryIcon`: URL of the icon displayed next to the article title in the section.

<br/>

### [Important notes](notes)

- **Exact match of values**: The value of the `category` property in the article must exactly match one of the values in the `categories` list.
  Mismatch will result in the article not being displayed in the correct section on the main page.
- **Order of sections**: The order of sections on the main page strictly follows the order of elements in the `categories` list.
- **Optionality**: If the property is not specified, the sections on the main page will not be displayed regardless of the values specified
  in the `category` meta properties for the articles.
- **Localization**: Each language directory must have its own `categories`, allowing for translations of section names
  into different languages.

<br/>

### [When to Use](when-to-use)

- **Content Organization**: When you need to structure the main page for better navigation and grouping articles by topics.
- **Improving User Experience**: To facilitate users in finding information by providing them with thematically grouped sections.

<br/>

### [Usage Tips](advice)

- **Plan the Structure in Advance**: Define the necessary categories and their order before filling in the content.
- **Consistent Naming**: Make sure the values of `category` in articles exactly match the values in `categories`, including case and spaces.
- **Updating Categories**: When adding new categories or changing the structure, remember to update the `categories` list in the language `metadata.md`.
- **Category Localization**: When translating into other languages, ensure that the categories align with the language preferences of the audience.

<br/>

## [Conclusion](conclusion)

The `categories` property is a key tool for structuring the main documentation page. Proper use of this property, combined with other metadata properties, allows for creating intuitive navigation and enhances the overall user experience interacting with the documentation.

<br/>

## [Usage Examples](examples)

### Example 1: Defining Categories in the Language Section

File: `ru/metadata.md`

```markdown
---
displayName: Russian
published: true
categories:
  - Getting Started
  - Services
  - Resource Settings
  - FAQ
---
```

**Description**:

- Defines four sections on the main page: "Getting Started," "Services," "Resource Settings," and "FAQ."
- The order of sections on the main page will correspond to the order in the `categories` array.

<br/>

### Example 2: Associating an Article with a Category

File: `ru/documentation/start.md`

```markdown
---
id: 1
title: Start Page
displayName: Start Page
published: true
order: 10
category: Getting Started
categoryName: Quick Start
categoryDescription: Learn how to get started with our application.
categoryOrder: 10
categoryIcon: /icons/start.svg
---

# Start Page

Welcome! Here you will find information on how to get started.
```

Description:

- `category`: "Getting Started" - links the article to a section on the main page.
- `categoryName`: "Quick Start" - the name of the article in the section on the main page.
- `categoryDescription`: A brief description to display below the article title.
- `categoryOrder`: The position of the article within the "Getting Started" section.
- `categoryIcon`: The path to the icon displayed next to the article title.

<br/>

### Example 3: Multiple Language Sections

File: `en/metadata.md`

```markdown
---
displayName: English
published: true
categories:
  - Getting Started
  - Services
  - Resource Settings
  - FAQ
---
```

Article File: `en/documentation/start.md`

```markdown
---
id: 1
title: Start Page
displayName: Start Page
published: true
order: 10
category: Getting Started
categoryName: Quick Start
categoryDescription: Learn how to get started with our application.
categoryOrder: 10
categoryIcon: /icons/start.svg
---

# Start Page

Welcome! Here you'll find information on how to get started.
```

Description:

- Ensures consistency in structure across different languages.
- Categories and articles are localized to match the language.
