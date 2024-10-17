---
id: 6
title: Footer - Documentation Interface
displayName: Footer
order: 30
published: true
historyName: Documentation Footer
historyDescription: The documentation footer enhances navigation by providing quick access to key sections through meta properties.
headerName: Documentation Footer
headerOrder: 2
footerName: Documentation Footer
footerOrder: 2
category: Services
categoryName: Documentation Footer
categoryDescription: The documentation footer enhances navigation by providing quick access to key sections through meta properties.
categoryOrder: 2
categoryIcon: https://img.solarspace.pro/docs/users.svg
---

# Documentation Footer

The documentation footer is one of the key elements of the interface. It provides users with quick access to main sections and functions, improves navigation, and contributes to the overall look of the documentation. In this article, we will examine in detail the role of the documentation footer, ways to customize it using meta properties, and examples of its usage.

![Footer](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/footer.png)

<br/>

## [Basic Functions](basic-functions)

- **Navigation:** Provides users with access to key sections and articles from any documentation article.
- **Consistency:** Creates a unified style and structure, making it easier for users to navigate through the documentation.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

- **`footerName`:** Sets the name of the link to the article in the footer.
  ![Impact of the footerName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/footer-name.png)

- **`footerOrder`:** Determines the order in which the link is displayed in the footer.
  ![Impact of the footerOrder property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/footer-order.png)

- **`published`:** Controls the visibility of the article in all interface elements, including the footer.

<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- **Link Display:** To display a link to an article in the footer, both properties `footerName` and `footerOrder` must be specified.
- **Order of Links:** Links in the footer are sorted in ascending order of the `footerOrder` value.
- **Article Visibility:** If `published` is set to `false`, the article will not be displayed, regardless of other meta properties.

<br/>

## [Step-by-By-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Select Articles for Footer Display

Identify key articles that users should have quick access to. These can include:

- Getting Started guides.
- API documentation.
- Support or contact sections.
- Frequently Asked Questions (FAQ).

### Step 2: Setting Meta Properties

Add the properties `footerName` and `footerOrder` to the metadata of the selected articles. Example:

```md
---
title: Getting Started
displayName: Introduction
order: 1
published: true
headerName: Start
headerOrder: 10
---
```

### Step 3: Check `published` Values

Ensure that the `published` property is set to `true` for the articles to be displayed in the footer and accessible to users.

### Step 4: Display Testing

After configuring the meta properties, check how the links are displayed on various devices and screens:

- Confirm that the links are displayed in the correct order.
- Verify the accuracy of link names and their relevance to the content.
- Ensure that the footer design is not compromised due to long names or a large number of links.

<br/>

## [Recommendations](recommendations)

### Optimal Number of Links

- **Avoid Footer Overload:** It is recommended to place no more than 7 links to maintain a clean and understandable design.
- **Priority:** Choose the most important and sought-after sections.

### Conciseness and Clarity of Names

- **Use Short Names:** This ensures better readability and prevents display issues on mobile devices.
- **Clarity:** Names should accurately reflect the content of the article or section.

### Consistency and Coherence

- **Unified Style:** Maintain consistency in the style and wording of link names.
- **Logical Order:** Arrange links in an order that corresponds to their importance or logical sequence of use.

<br/>

### Testing and Responsive Design

- **Testing on Different Devices:** Make sure the footer displays correctly on desktops, tablets, and smartphones.
- **Responsiveness:** The footer should be user-friendly on screens of various sizes.

<br/>

## [Usage Examples](examples)

### Example 1: Standard Footer with Key Sections

**Articles and their meta properties:**

- **Article "Getting Started":**

```md
---
title: Getting Started
displayName: How to Begin
order: 1
published: true
footerName: Getting Started
footerOrder: 10
---
```

- **Article "Articles":**

```md
---
title: Articles
displayName: Articles
order: 2
published: true
footerName: Articles
footerOrder: 20
---
```

- **Article "Questions":**

```md
---
title: Questions
displayName: Questions
order: 3
published: true
footerName: Questions
footerOrder: 30
---
```

- **Article "Hidden Section":**

```md
---
title: Hidden Section
displayName: Hidden Section
order: 4
published: false
footerName: Hidden Section
footerOrder: 40
---
```

- **Article "Support":**

```md
---
title: Support
displayName: Support
order: 5
published: true
footerName: Support
footerOrder: 50
---
```

**Result in the footer:**

- Getting Started
- Articles
- Questions
- Support

<br/>

### Example 2: Footer Highlighting New Features

**Article "New Features":**

```md
---
title: New Features in Version 3.0
displayName: New Features
order: 4
published: true
footerName: What's New
footerOrder: 5
---
```

**Result:**

- The "What's New" link will be displayed first in the footer, drawing users' attention to the latest updates.

<br/>

## [Conclusion](conclusion)

The footer is an important element that impacts usability. Proper configuration using the meta properties `footerName` and `footerOrder` allows for quick access to key sections and enhances navigation.

<br/>

## [Additional Resources](additional-resources)

- [Detailed description of the meta property `footerName`](38)
- [Detailed description of the meta property `footerOrder`](39)
- [Detailed description of the meta property `published`](46)
