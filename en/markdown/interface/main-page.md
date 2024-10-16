---
id: 9
title: Main Sections - Documentation Interface
displayName: Main Sections
order: 10
published: true
historyName: Main Sections of Documentation
historyDescription: Structures content, simplifies navigation, and helps users find important articles and sections.
---

# Main Sections of the Homepage

The main sections of the documentation homepage are organized blocks of content displayed on the main page. They are designed to structure information, making it easier for users to find and access the most important sections and articles. Each section may contain one or more articles that are related by the `categories` meta property of the language section and the `category` property of a specific article.

![Main Sections of the Homepage](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/main-page-blocks.png)

<br/>

## [Basic Functions](basic-functions)

- **Content Organization:** Sections allow you to divide the documentation into logical categories specified in the `categories` field, such as `Getting Started`, `Services`, `Resource Settings`, `FAQ`. Using the `category` property, you can select one of the sections specified in `categories` where the content will be displayed.
- **Simplified Navigation:** Users can quickly find the sections they need and navigate to them without wasting time searching for information.
- **Visual Differentiation:** Different sections can have their own icons and descriptions, making the interface more understandable.
- **Content Priority:** By the display order, you can highlight the most important or current sections.
- **Adaptability:** Sections are adapted for various devices, providing convenient access on both desktops and mobile devices.

<br/>

## [Customization Using Meta Properties](customization-using-meta-properties)

To configure the main sections of the documentation homepage, specific meta properties are used, which are specified at the beginning of Markdown files. These properties allow you to determine which sections will be present, in which section an article will be placed, how it will be displayed, and in what order it will be positioned.

### Main meta properties for sections:

- **`categories`**: Defines the names and order of sections on the main page in the language `metadata.md` file, where the article will be displayed. Example:
```markdown
---
displayName: English
published: true
categories:
  - Getting Started
  - Services
  - Resource Configuration
  - FAQ
---
```
![Impact of the category property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category.png)
- **`category`**: Defines the section on the main page where the article will be displayed. Examples: `Getting Started`, `Services`, `Resource Configuration`, `FAQ`.
- **`categoryName`**: The name of the article in the section on the main page.
![Impact of the categoryName property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-name.png)
- **`categoryDescription`**: A brief description of the article to display in the section.
![Impact of the categoryDescription property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-description.png)
- **`categoryOrder`**: The order of displaying the article within the section.
![Impact of the categoryOrder property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-order.png)
- **`categoryIcon`**: The icon displayed next to the article name in the section.
![Impact of the categoryIcon property](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-icon.png)

### Example metadata for an article:

```md
---
title: Quick Start
displayName: Getting Started
order: 1
published: true
category: Getting Started
categoryName: Quick Start
categoryDescription: Quick start with our service.
categoryOrder: 10
categoryIcon: /icons/quickstart.svg
---

# Quick Start

Welcome to the quick start guide...```


<br/>

## [Impact of Meta Properties](impact-of-meta-properties)

- `published` determines whether the article will be displayed even if all the necessary properties are specified.
- `categories` defines the list of sections on the homepage.
- `category` determines which section of the homepage the article will be placed in. `category: Getting Started` places the article in the "Getting Started" section.
- `categoryName` sets the name of the article in the section. `categoryName: Quick Start` displays the name "Quick Start" in the respective section.
- `categoryDescription` provides a brief description of the article to be displayed in the section. `categoryDescription: Quick start with our service` displays the description below the article name.
- `categoryOrder` determines the display order of the article within the `Getting Started` section. `categoryOrder: 10` positions the article before the one with `categoryOrder: 20`.
- `categoryIcon` specifies the path to the icon that will be displayed next to the article name. `categoryIcon: /icons/quickstart.svg` displays the "quickstart.svg" icon next to the article name.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Organizing Sections

Define the sections that will be displayed on the homepage.

### Step 2: Defining Section

Decide in which section the documentation article will be located.

### Step 3: Setting Meta Properties in Files

Add the necessary meta properties in the `metadata.md` of the language section and each Markdown file to define sections, document placement within the section, and display order.

**Example:**

```md
---
title: Deep Dive
displayName: Advanced Usage
order: 2
published: true
category: Getting Started
categoryName: Deep Dive
categoryDescription: For experienced users
categoryOrder: 20
categoryIcon: /icons/deepdive.svg
---

# Deep Dive

In this guide, we will delve into...
```

### Step 4: Setting Icons and Descriptions

Ensure that the paths to icons are correct and the descriptions are concise and informative.

### Step 5: Generating and Checking the Website

After configuring the meta properties, check how the links are displayed on the homepage on various devices and screens:

- Make sure that the links are displayed in the correct order.
- Check the correctness of the link names and their relevance to the content.
- Ensure that the design is not disrupted due to long names or a large number of links.

<br/>

## [Recommendations](recommendations)

- **Use clear titles:** Section and article titles should be intuitive for users.
- **Optimize the order:** By arranging articles in order of importance or logical sequence, you improve navigation.
- **Maintain consistency:** Use a consistent style for naming and descriptions across all sections.
- **Icons:** Choose icons that match the theme of the article to enhance visual perception.
- **Concise descriptions:** Descriptions should be brief (up to 30 characters) to fully display on the main page.
- **Plan the structure:** Think ahead about which sections and articles will be included to avoid frequent changes.

<br/>

## [Usage Examples](examples)

### Example 1: Sections "Getting Started" and "Services"

**File `quickstart.md`:**

```md
---
title: Quick Start
displayName: Getting Started
order: 1
published: true
category: Getting Started
categoryName: Quick Start
categoryDescription: Learn how to quickly start using our service
categoryOrder: 10
categoryIcon: /icons/quickstart.svg
---

# Quick Start

Welcome to the quick start guide...
```

**File `advanced-use.md`:**

```md
---
title: Advanced Usage
displayName: Advanced Usage
order: 1
published: true
category: Getting Started
categoryName: Advanced Usage
categoryDescription: Advanced usage of the service
categoryOrder: 20
categoryIcon: /icons/advanced-use.svg
---
# Quick Start

Welcome to the quick start guide...
```

**File `consulting.md`:**

```md
---
title: Consulting
displayName: Consulting
order: 3
published: true
category: Services
categoryName: Consulting
categoryDescription: Professional consultations for your business
categoryOrder: 10
categoryIcon: /icons/consulting.svg
---

# Consulting

We offer expert consultations in the field of...
```

**File `support.md`:**

```md
---
title: Technical Support
displayName: Technical Support
order: 3
published: true
category: Services
categoryName: Technical Support
categoryDescription: Read if you have questions
categoryOrder: 10
categoryIcon: /icons/support.svg
---

# Consulting

We offer expert consultations in the field of...
```

**Result on the main page:**

- **Getting Started**
  - Quick Start
  - Advanced Usage
- **Services**
  - Consulting
  - Technical Support

<br/>

### Example 2: Hiding a Section from Sections

**File `drafts.md`:**

```md
---
title: Drafts
displayName: Drafts
order: 99
published: false
category: Services
categoryName: Drafts
categoryDescription: Unfinished sections and articles
categoryOrder: 1
categoryIcon: /icons/drafts.svg
---

# Drafts

_This section is under development and will be available later._
```

**Result:** The document "Drafts" is not displayed on the main page because `published: false`.

<br/>

## [Conclusion](conclusion)

Sections on the documentation main page play an important role in organizing and presenting content, providing convenient navigation and access to key sections.
Proper configuration of sections using meta properties allows you to create a structured and intuitive interface. By following recommendations and examples,
you can optimize the main documentation page for easier article search.

<br/>

## [Additional Resources](additional-resources)

- [Detailed description of the meta property `published`]([46])
- [Detailed description of the meta property `categories`]([30])
- [Detailed description of the meta property `category`]([31])
- [Detailed description of the meta property `categoryName`]([34])
- [Detailed description of the meta property `categoryDescription`]([32])
- [Detailed description of the meta property `categoryOrder`]([35])
- [Detailed description of the meta property `categoryIcon`]([33])
```
