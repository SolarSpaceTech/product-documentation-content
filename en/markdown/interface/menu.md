---
id: 10
title: Menu - Documentation Interface
displayName: Menu
order: 40
published: true
historyName: Documentation Menu
historyDescription: The documentation menu simplifies navigation and section structure using the `displayName`, `order`, `published` meta properties.
---

# Documentation Menu

The documentation menu is one of the key elements of the user interface. It provides structure and navigation through sections and articles, allowing users to easily find and access the necessary information. The menu is displayed in the sidebar and reflects the hierarchical structure of the documentation.

![Menu](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/menu.png)

<br/>

## [Basic Functions](basic-functions)

- **Navigation:** Provides quick access to sections and sub-articles, making it easier to find the required information.
- **Content Structuring:** Displays the hierarchical organization of the documentation, showing the relationship between different sections.
- **Orientation:** Helps users understand where they are in the documentation structure by highlighting the current section or article.
- **Accessibility:** Makes all documentation accessible from any documentation article.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

The documentation menu is customized using the following meta properties specified in the Markdown file metadata:

- **`displayName`:** Defines the name of the section or article displayed in the menu and breadcrumbs.
  ![Impact of the displayName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/display-name.png)
- **`order`:** Specifies the display order of sections and articles in the menu.
  ![Impact of the order property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/order.png)
- **`published`:** Controls the visibility of a section or article in the menu and navigation. If set to `false`, the item is not displayed.

<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- `displayName` is used as the name of the menu item and breadcrumb item.
- `order` sorts menu items in ascending order of value.
- `published` if set to `false`, the section or article will not be displayed in the menu and navigation. Nested items will not be displayed if the parent section has `published: false`.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Structuring the File System

- Organize Markdown files in directories and subdirectories that reflect the documentation hierarchy.
- Ensure that each section has its own `metadata.md` file with metadata description.

### Step 2: Configuring Meta Properties in Files

**Example metadata for a section:**

```md
---
displayName: Guide
order: 1
published: true
---
```

**Example metadata for an article:**

```md
---
title: Product Installation
displayName: Installation
order: 1
published: true
---
```

### Step 3: Defining the Order of Elements

- Set `order` values for sections and articles to determine their sequence in the menu.
- Use steps between values (e.g., 10, 20, 30) to facilitate adding new elements.

### Step 4: Managing Visibility

- Use the `published` property to control the display of items in the menu.
- To hide a section or article, set `published: false`.

### Step 5: Testing the Menu

- Generate the site and check that the menu displays correctly.
- Ensure that all links work and lead to the corresponding sections and articles.

<br/>

## [Recommendations](recommendations)

- **Consistent Naming:** Use clear and concise names in `displayName` to enhance the user experience.
- **Logical Structure:** Organize content in a logical hierarchy that reflects the theme and learning sequence.
- **Unique `order` Values:** Assign unique `order` values within the same menu level for precise control of display order.
- **Planning:** Plan the menu structure in advance to avoid frequent changes and reordering.

<br/>

## [Usage Examples](examples)

### Example 1: Creating a Multi-level Menu

**File Structure:**

- `/`
  - `metadata.md` (Main)
  - `/getting-started/`
    - `metadata.md` (Section "Getting Started")
    - `installation.md` (Article "Installation")
    - `configuration.md` (Article "Configuration")
  - `/guides/`
    - `metadata.md` (Section "Guides")
    - `advanced-usage.md` (Article "Advanced Usage")

**Metadata for the "Getting Started" section:**

```md
---
displayName: Getting Started
order: 1
published: true
---
```

**Metadata for the "Installation" article:**

```md
---
title: Product Installation
displayName: Installation
order: 1
published: true
---
```

**Metadata for the "Guides" section:**

```md
---
displayName: Guides
order: 2
published: true
---
```

<br/>

### Example 2: Hiding a Section from the Menu

**Metadata for the "Drafts" section:**

```md
---
displayName: Drafts
order: 99
published: false
---
```

**Result:** The "Drafts" section and all its articles are not displayed in the menu and navigation.

<br/>

## [Conclusion](conclusion)

Documentation menu plays a critical role in providing convenient and efficient site navigation. By using the meta properties `displayName`, `order`, and `published`,
you can customize the menu according to the audience's needs, ensuring a logical structure and sequence. Careful planning
and implementation will help create an easily usable interface.

<br/>

## [Additional Resources](additional-resources)

- [Detailed description of the meta property `displayName`]([37])
- [Detailed description of the meta property `order`]([45])
- [Detailed description of the meta property `published`]([46])
