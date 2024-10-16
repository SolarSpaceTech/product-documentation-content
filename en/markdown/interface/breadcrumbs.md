---
id: 4
title: Breadcrumbs - Documentation Interface
displayName: Breadcrumbs
order: 50
published: true
historyName: Breadcrumbs Documentation
historyDescription: The documentation menu simplifies navigation and section structure using the `displayName`, `order`, `published` meta properties.
headerName: Breadcrumbs
headerOrder: 4
footerName: Breadcrumbs
footerOrder: 4
category: FAQ
categoryName: Breadcrumbs
categoryDescription: The documentation menu simplifies navigation and section structure using the `displayName`, `order`, `published` meta properties.
categoryOrder: 4
categoryIcon: https://img.solarspace.pro/docs/waf.svg
---

# Breadcrumbs Documentation

Breadcrumbs are a navigational element of the interface that displays the user's path from the main page to the current article. This interface element helps users understand the documentation structure. It is displayed at the top of the page between the header and the article.

![Breadcrumbs](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/breadcrumbs.png)

<br/>

## [Basic Functions](basic-functions)

- **Hierarchy Navigation:** Displays the path from the main page to the current article, reflecting the structure of sections and sub-articles.
- **Orientation Improvement:** Helps users understand where they are in the overall documentation structure.
- **Enhancing User Experience:** Reduces the level of user "lostness" when browsing deeply nested sections.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

The following meta properties are used to customize breadcrumbs in the documentation:

- **`displayName`:** Determines the name of the section or article displayed in the breadcrumbs.
  ![Impact of the displayName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/display-name.png)

<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- The `displayName` is used in breadcrumbs to display the names of sections and articles.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Defining Documentation Structure {#step-1}

- Organize documentation in the file system using folders and files that reflect the hierarchy of sections and articles.

### Step 2: Setting Meta Properties in Files {#step-2}

**Example of section metadata:**

```md
---
displayName: Guides
order: 1
published: true
---
```

**Example of article metadata:**

```md
---
title: Product Installation
displayName: Installation
order: 1
published: true
---
```

### Step 3: Setting `displayName` for Convenience {#step-3}

- Provide clear and concise names in `displayName` to ensure informative breadcrumbs that do not take up too much space.

### Step 4: Testing Breadcrumbs {#step-4}

- Generate documentation and navigate to different articles to verify the correct display of breadcrumbs.
- Ensure that the path is displayed correctly.

<br/>

## [Recommendations](recommendations)

- **Concise Naming:** Use short and clear names in `displayName` for optimal display in breadcrumbs.
- **Consistent Style:** Maintain a consistent naming style throughout the documentation.
- **Avoid Deep Nesting Levels:** Try not to create overly deep hierarchies to prevent breadcrumbs from becoming too long.
- **Visibility Check:** Regularly check which sections and articles are displayed in breadcrumbs to avoid hidden or unnecessary elements.

<br/>

## [Usage Example](examples)

**File Structure:**

- `/ru`
  - `metadata.md` (Russian)
  - `/documentation`
    - `metadata.md` (Documentation)
    - `/getting-started/`
      - `metadata.md` (Section "Getting Started")
      - `installation.md` (Article "Installation")
      - `configuration.md` (Article "Configuration")

**Metadata for the section "Getting Started":**

```md
---
displayName: Getting Started
order: 1
published: true
---
```

**Metadata for the article "Installation":**

```md
---
title: Product Installation
displayName: Installation
order: 1
published: true
---
```

**Breadcrumbs Display on the "Installation" Page:**

```
Documentation / Getting Started / Installation
```

<br/>

## [Conclusion](conclusion)

Breadcrumbs are an important navigational element in documentation, improving user orientation and simplifying site navigation. Properly configuring breadcrumbs with the `displayName` meta property helps create a clear and efficient structure, facilitating access to the necessary information.

<br/>

## [Additional Resources](additional-resources)

- [Detailed description of the `displayName` meta property]([37])
