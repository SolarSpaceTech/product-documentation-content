---
id: 7
title: Documentation Header - Documentation Interface
displayName: Header
order: 20
published: true
historyName: Documentation Header
historyDescription: The site header provides quick access to key sections, improving navigation and customization through meta properties.
headerName: Documentation Header
headerOrder: 1
footerName: Documentation Header
footerOrder: 1
category: Getting Started
categoryName: Documentation Header
categoryDescription: The site header provides quick access to key sections, improving navigation and customization through meta properties.
categoryOrder: 1
categoryIcon: https://img.solarspace.pro/docs/microchip.svg
---

# Documentation Header

The documentation header is one of the key elements of the interface. It provides users with quick access to main sections and features, improves navigation, and contributes to the overall look of the documentation. In this article, we will examine in detail the role of the documentation header, methods of customization using meta properties, and usage examples.

![Header](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/header.png)

<br/>

## [Basic Functions](basic-functions)

- **Navigation:** Provides users with access to key sections and articles from any documentation article.
- **Search:** Includes a search bar that allows users to quickly find the information they need.
- **Consistency:** Creates a unified style and structure, making it easier for users to navigate the site.
- **Theming:** Allows the user to switch between dark and light themes.
- **Language:** Enables users to choose the language for content display.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

- **`headerName`:** Sets the name of the link to the article in the header.
  ![Effect of the headerName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/header-name.png)
- **`headerOrder`:** Determines the order of displaying the link in the header.
  ![Effect of the headerOrder property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/header-order.png)
- **`published`:** Controls the visibility of the article in all interface elements, including the header.

<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- **Link Display:** To display a link to an article in the header, both properties `headerName` and `headerOrder` must be specified.
- **Order of Links:** Links in the header are sorted in ascending order of the `headerOrder` value.
- **Article Visibility:** If `published` is set to `false`, the article will not be displayed, regardless of other meta properties.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Select Articles to Display in the Header

Identify key articles that users should have quick access to. These can include:

- Getting Started guides.
- API documentation.
- Support or contact sections.
- Frequently Asked Questions (FAQ).

### Step 2: Setting Meta Properties

Add the properties `headerName` and `headerOrder` to the metadata of the selected articles. Example:

```md
---
title: Getting Started
displayName: How to Begin
order: 1
published: true
headerName: Start
headerOrder: 10
---
```

### Step 3: Checking the `published` Values

Ensure that the `published` property is set to `true` for articles to be displayed in the header and accessible to users.

### Step 4: Display Testing

After configuring the meta properties, check how the links are displayed in the header on various devices and screens:

- Ensure that the links are displayed in the correct order.
- Check the accuracy of the link names and their relevance to the content.
- Ensure that the header design is not disrupted due to long names or a large number of links.

<br/>

## [Recommendations](recommendations)

### Optimal Number of Links

- **Avoid Header Overload:** It is recommended to place no more than 5 links to maintain a clean and understandable design.
- **Priority:** Choose the most important and in-demand sections.

### Conciseness and Clarity of Names

- **Use Short Names:** This ensures better readability and prevents display issues on mobile devices.
- **Clarity:** Names should accurately reflect the content of the article or section.

### Sequence and Consistency

- **Unified Style:** Maintain consistency in the style and wording of link names.
- **Logical Order:** Arrange links in order of importance or logical sequence of use.

### Testing and Responsive Design

- **Checking on Different Devices:** Make sure the header displays correctly on desktops, tablets, and smartphones.
- **Adaptability:** The header should be user-friendly on screens of different sizes.

<br/>

## [Usage Examples](examples)

### Example 1: Standard Header with Key Sections

**Articles and their meta properties:**

- **Article "Getting Started":**

```md
---
title: Getting Started
displayName: Getting Started
order: 1
published: true
headerName: Getting Started
headerOrder: 10
---
```

- **Article "Articles":**

```md
---
title: Articles
displayName: Articles
order: 2
published: true
headerName: Articles
headerOrder: 20
---
```

- **Article "Questions":**

```md
---
title: Questions
displayName: Questions
order: 3
published: true
headerName: Questions
headerOrder: 30
---
```

- **Article "Hidden Section":**

```md
---
title: Hidden Section
displayName: Hidden Section
order: 4
published: false
headerName: Hidden Section
headerOrder: 40
---
```

- **Article "Support":**

```md
---
title: Support
displayName: Support
order: 5
published: true
headerName: Support
headerOrder: 50
---
```

**Result in the header:**

- Getting Started
- Articles
- Questions
- Support

<br/>

### Example 2: Header Emphasizing New Features

**Article "New Features":**

```md
---
title: New Features in Version 3.0
displayName: New Features
order: 4
published: true
headerName: What's New
headerOrder: 5
---
```

**Result:**

- The "What's New" link will be displayed first in the header, drawing users' attention to the latest updates.

<br/>

## [Conclusion](conclusion)

The header is an important element that affects usability. Properly configuring the header using the meta properties `headerName` and `headerOrder` allows for quick access to key sections and improves navigation.

<br/>

## [Additional Resources](additional-resources)

- [Detailed description of the `headerName` meta property]([40])
- [Detailed description of the `headerOrder` meta property]([41])
- [Detailed description of the `published` meta property]([46])
