---
id: 37
title: displayName Description - General - Meta properties
displayName: displayName
order: 30
published: true
historyName: Description of the displayName meta property
historyDescription: The displayName meta property sets a brief title for the article to be displayed in the menu and documentation navigation.
---

# displayName Property

**Meta property:** `displayName`

**Data type:** String

**Scope of influence:**
![Property Influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/display-name.png)


<br/>

## [Description](description)

The `displayName` meta property is used to specify the name of an article or section that will be displayed in the documentation navigation elements,
such as the menu and breadcrumbs. This property plays a key role in organizing and presenting documentation, helping users quickly
navigate and find the sections or articles they need.

<br/>

### [Basic Functions](basic-functions)

- **Menu Display:** The `displayName` value is used as the menu item name for the corresponding article or section, allowing
users to see clear and convenient names when navigating through the documentation.
- **Breadcrumbs:** In breadcrumbs, which show the user's path through the documentation structure, `displayName` is displayed at each
level, providing a clear representation of the current location.
- **Structure Organization:** Helps structure the documentation, providing logical and consistent section and article names.

<br/>

### [Working with Other Meta Properties](with-other-properties)

- **`title`:** While `title` is displayed on the browser tab and may be more detailed or contain additional information,
`displayName` is usually shorter and intended for quick perception in navigation elements.
- **`order`:** Determines the display order of the article or section in the menu, but does not affect `displayName`.
- **`published`:** Determines whether the article or section will be displayed in the menu and other navigation elements. If `published` is set
to `false`, the item will not be displayed, regardless of the `displayName` value.
- **`headerName` and `footerName`:** Used to display the article name in the site header and footer, respectively, and may differ from `displayName`.
- **`historyName`:** Used to display the article name in the history block, may differ from `displayName`.
- **`categoryName`:** Used to display the article name in one of the sections with articles on the main page, may differ from `displayName`.


<br/>

### [Important Notes](notes)

- **Conciseness and Clarity:** It is recommended to use short and clear names in `displayName` to facilitate navigation and improve the user experience.
- **Consistency:** Maintain a consistent writing style for `displayName` throughout the documentation for a professional look and ease of use.
- **Uniqueness:** Ensure that each `displayName` value is unique within the context of the parent section to avoid confusion.

<br/>

### [When to Use](when-to-use)

- **Always when creating an article or section:** This is the primary property for displaying the title in the menu and breadcrumbs.
- **For simplifying navigation:** When it is necessary to provide users with clear and concise names for quick access to documentation sections.
- **For shortening long titles:** If the `title` is too long or contains details unnecessary in the menu, `displayName` can be used to provide a brief version.

<br/>

### [Usage Tips](advice)

- **Use clear terms:** Names should be intuitive for the target audience.
- **Avoid redundancy:** Do not include unnecessary words or phrases in `displayName`.
- **Follow documentation style:** Use a consistent case and writing form (e.g., all names in singular form).
- **Conciseness:** Strive for a short name, usually no more than 2-3 words.
- **Informativeness:** The name should accurately reflect the content of the section or article.
- **Consistency:** Use the same writing style throughout the documentation (e.g., all names in imperative mood
  or in noun form).

<br/>

## [Conclusion](conclusion)

The `displayName` meta property is an important element in generating documentation, as it directly affects how users will navigate your site. Proper and thoughtful use of `displayName` enhances the usability of the documentation, making it more accessible and understandable for users.

<br/>

## [Usage Examples](examples)

### Example 1: Article on Setting Up Development Environment

```md
---
title: Setting Up Development Environment for the Project
displayName: Setting Up Environment
order: 2
published: true
---
# Setting Up Development Environment

This section describes how to set up the environment for developing our project...
```

- **`displayName`:** "Setting Up Environment" will be displayed in the menu and breadcrumbs, providing a brief and clear title.
- **`title`:** "Setting Up Development Environment for the Project" will be displayed on the browser tab, providing a more detailed description.

<br/>

### Example 2: Section with Multiple Subarticles

**`metadata.md` File for the Section:**

```md
---
displayName: Guides
order: 1
published: true
---
```

**Article File `installation.md`:**

```md
---
title: Product Installation - Step-by-Step Guide
displayName: Installation
order: 1
published: true
---
# Product Installation

Follow these steps to install our product...
```
