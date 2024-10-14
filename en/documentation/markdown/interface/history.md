---
id: 8
title: Visit History - Documentation Interface
displayName: Visit History
order: 70
published: true
historyName: Documentation Visit History
historyDescription: Enhances navigation by allowing quick access to previously viewed articles and sections.
---

# Documentation Visit History

The documentation visit history is a user interface element that displays a list of recently viewed articles or sections by the user. This feature allows for quick return to previously studied content, improving navigation and enhancing the usability of the documentation. It is located at the bottom of the page, providing easy access to past views without the need to search for them again.

![Visit History](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/history.png)

<br/>

## [Basic Functions](basic-functions)

- **Quick access to previously viewed content:** Allows users to instantly return to articles of interest without the need for repeated searching.
- **Personalization of experience:** Displays individual visit history for each user, making interaction with the documentation more personalized.
- **Navigation improvement:** Facilitates movement through the documentation, especially when exploring deep or complex sections.
- **Reduction of search time:** Decreases the time needed to find previously studied material, increasing the efficiency of using the documentation.
- **Multitasking support:** Helps users work with multiple documentation sections simultaneously, easily switching between them.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

The following meta properties are used to customize the visit history block in the documentation:

- **`id`**: Sets a unique identifier for the article, stored client-side in the viewing history.
- **`historyName`**: Sets the name of the article in the visit history block.
  ![Impact of the historyName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/history-name.png)
- **`historyDescription`**: Provides a brief description of the article in the visit history block.
  ![Impact of the historyDescription property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/history-description.png)
- **`published`**: Controls the visibility of the article in all interface elements, including the visit history block.

### Example metadata for an article:

```md
---
id: 1000
title: User Management in the System
displayName: User Management
order: 4
published: true
historyName: User Management
historyDescription: How to add, delete, and edit users in the system
---

# User Management in the System

This section describes methods for managing users...
```

<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- `id` defines the identifier used to retrieve `historyName` and `historyDescription` for the article.
- `historyName` specifies the article title displayed in the visit history block.
- `historyDescription` provides a brief description of the article in the visit history block.
- `published` controls the visibility of the article in all interface elements, including the visit history block. It allows hiding unpublished or temporarily
  unavailable articles without deleting them from the file structure.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Adding Meta Properties to Markdown Files

For each article, add the following properties to its metadata:

- **`id`**: Unique identifier.
- **`historyName`**: Name for the visit history.
- **`historyDescription`**: Brief description for the visit history.
- **`published`**: Ensure it is set to `true`.

**Example:**

```md
---
title: Administrator's Guide
displayName: Administrator
order: 5
published: true
historyName: Administrator's Guide
historyDescription: Comprehensive guide to system management
---

# Administrator's Guide

In this section, you will find information about...
```

### Step 2: Checking the Correctness of Meta Properties

Ensure that all necessary meta properties are correctly specified and do not contain errors.

### Step 3: Generating and Testing the Site

Generate the documentation and navigate to different articles to verify the correct display.

<br/>

## [Recommendations](recommendations)

- **Conciseness and Clarity:** Write concise and clear titles and descriptions for the visit history to help users quickly understand the article content.
- **Consistency:** Maintain a consistent writing style for titles and descriptions across all articles.
- **Optimal Length:** Limit the length of `historyDescription` to 120 characters to avoid text truncation in the interface.

<br/>

## [Usage examples](examples)

### Example 1: Article with custom title and description in visit history

**File `user-management.md`:**

```md
---
id: 1000
title: User Management in the System
displayName: User Management
order: 4
published: true
historyName: Users
historyDescription: How to add, delete, and edit users in the system
---

# User Management in the System

This section describes methods for managing users...
```

**Result:**

If the user has previously visited this page, the visit history block will display:

- **Users**
- _How to add, delete, and edit users in the system_

<br/>

### Example 3: Hiding an article from the visit history

**File `draft-feature.md`:**

```md
---
id: 1001
title: Draft Feature
displayName: Draft Feature
order: 10
published: false
historyName: Draft Feature
historyDescription: This feature is under development and will be available later
---

# Draft Feature

_This article is under development and will be published soon._
```

**Result:**

The article "Draft Feature" will not be displayed in the visit history block due to `published: false`, even if the user has visited this page before and it later became unpublished.

---

## [Conclusion](conclusion)

The documentation visit history is an important tool for improving navigation. It allows users to quickly revisit previously studied materials, increasing the efficiency of using the documentation. Proper configuration using meta properties: `id`, `historyName`, `historyDescription`, and `published` ensures accurate display of the necessary information and contributes to creating an intuitively understandable interface.

---

## [Additional Resources](additional-resources)

- [Detailed description of the meta property `id`]([44])
- [Detailed description of the meta property `published`]([46])
- [Detailed description of the meta property `historyName`]([43])
- [Detailed description of the meta property `historyDescription`]([42])

Please provide me with the Markdown document that needs to be translated from Russian to English.
