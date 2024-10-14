---
id: 39
title: Description of footerOrder - Footer - Meta properties
displayName: footerOrder
order: 150
published: true
historyName: Description of the meta property footerOrder
historyDescription: The meta property footerOrder determines the order of displaying links in the documentation footer, improving navigation and access to important sections.
---

# Property footerOrder

**Meta property:** `footerOrder`

**Data type:** Number

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/footer-order.png)

<br/>

## [Description](description)

The meta property `footerOrder` is used to determine the order of displaying links to articles in the documentation footer. The footer serves as a key element
of navigation, providing quick access to the most important sections or articles. With `footerOrder`, you can precisely configure the sequence of links
in the footer, ensuring logical and user-friendly navigation.

<br/>

### [Basic Functions](basic-functions)

- **Managing the order of links in the footer:** The value of `footerOrder` determines the position of the article link in the documentation footer.
  Links with a lower `footerOrder` value are displayed to the left or above (depending on the screen resolution).
- **Priority of display:** Allows arranging links by importance, providing users with the most relevant content first.
- **Customization flexibility:** Provides control over the footer structure, allowing it to be adapted to documentation needs.

<br/>

### [How it works with other meta properties](with-other-properties)

- **With `footerName`:** To display a link in the footer, both properties must be specified: `footerName` sets the link name, and `footerOrder` determines its position.
- **With `published`:** If `published` is set to `false`, the article will not be displayed in the footer, regardless of the values of `footerName` and `footerOrder`.
- **With other meta properties:** Does not affect the display of the article in the menu, footer, or other interface elements, such as `order` or `footerOrder`.

<br/>

### [Important Notes](notes)

- **Mandatory:** To display an article in the footer, both properties `footerName` and `footerOrder` must be specified. The absence of either will result in the link not appearing in the footer.
- **Value Range:** `footerOrder` accepts integer values. It is recommended to use positive numbers for clarity and ease of management.
- **Uniqueness of Values:** Not mandatory, but recommended for the values of `footerOrder` to be unique for precise control of the display order.
- **Sorting:** Links in the footer are sorted in ascending order of the `footerOrder` value. Links with lower values are displayed first.

<br/>

### [When to Use](when-to-use)

- **When Configuring Documentation Footer:** To determine the sequence of link display and ensure logical navigation.
- **For Content Prioritization:** When arranging links by importance, providing users with the most sought-after sections first.
- **When Updating Documentation:** To add new links to the footer without disrupting the existing order.

<br/>

### [Usage Tips](advice)

- **Incremental Step:** Use a step of 5 or 10 between `footerOrder` values for ease of adding new links.
- **Consider Importance:** Place the most important links at the beginning of the footer, assigning them lower `footerOrder` values.
- **Testing:** Check how links are displayed on different devices and screens to ensure the correctness of the order and ease of use.
- **Step Between Values:** Use a step (e.g., 10, 20, 30) between `footerOrder` values to allow for inserting new links between existing ones without the need to renumber all elements.
- **Structure Planning:** Plan in advance which sections or articles should be accessible from the footer and determine their order.
- **Consistency:** Adhere to a consistent numbering scheme and naming style.

<br/>

## [Conclusion](conclusion)

The meta property `footerOrder` is a key tool for managing the order of links displayed in the documentation footer. Proper use of this property allows for creating a logical and intuitive navigation, improving user experience, and facilitating access to important information. Plan the footer structure and use `footerOrder` in conjunction with `footerName` for effective interface customization.

<br/>

## [Usage Examples](examples)

### Example 1: Configuring the Order of Links in the Footer

**Article 1:**

```md
---
title: Getting Started
displayName: Introduction
order: 1
published: true
footerName: Getting Started
footerOrder: 10
---

# Getting Started

Welcome to our getting started guide...
```

**Article 2:**

```md
---
title: API Documentation
displayName: API
order: 2
published: true
footerName: API
footerOrder: 20
---

# API Documentation

This section describes the available API methods...
```

**Article 3:**

```md
---
title: Support
displayName: Support
order: 3
published: true
footerName: Support
footerOrder: 30
---

# Support

If you have any questions, contact our support team...
```

**Result in the documentation footer:**

1. Getting Started (footerOrder: 10)
2. API (footerOrder: 20)
3. Support (footerOrder: 30)

<br/>

### Example 2: Omitting the `footerOrder` Value

**Article:**

```md
---
title: Blog
displayName: Blog
order: 4
published: true
footerName: Blog
---

# Blog

Read the latest news and updates...
```

**Result:** Since `footerOrder` is not specified, the link to the "Blog" article will not be displayed in the documentation footer.
