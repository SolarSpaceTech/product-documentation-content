---
id: 41
title: Description of headerOrder - Header - Meta properties
displayName: headerOrder
order: 130
published: true
historyName: Description of the meta property headerOrder
historyDescription: The meta property headerOrder defines the order of displaying links in the documentation header, improving navigation and access to important sections.
---

# Property headerOrder

**Meta property:** `headerOrder`

**Data type:** Number

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/markdown/images/header-order.png)

<br/>

## [Description](description)

The meta property `headerOrder` is used to define the order of displaying links to articles in the documentation header. The header serves as a key
navigation element, providing quick access to the most important sections or articles of the documentation.
With `headerOrder`, you can precisely configure the sequence of links in the header, ensuring logical and user-friendly navigation.

<br/>

### [Basic Functions](basic-functions)

- **Managing the order of links in the header:** The value of `headerOrder` determines the position of the article link in the documentation header.
  Links with a lower `headerOrder` value are displayed to the left or above (depending on the screen resolution).
- **Priority of display:** Allows arranging links by importance, providing users with the most relevant content first.
- **Customization flexibility:** Provides control over the header structure, allowing it to be adapted to the documentation needs.

<br/>

### [How it works with other meta properties](with-other-properties)

- **With `headerName`:** To display a link in the header, both properties must be specified: `headerName` sets the link name, and `headerOrder` determines its position.
- **With `published`:** If `published` is set to `false`, the article will not be displayed in the header, regardless of the values of `headerName` and `headerOrder`.
- **With other meta properties:** Does not affect the display of the article in the menu, footer, or other interface elements, such as `order` or `footerOrder`.

<br/>

### [Important Notes](notes)

- **Mandatory:** To display an article in the header, both properties `headerName` and `headerOrder` must be specified. The absence of one of them will result in the link not appearing in the header.
- **Value Range:** `headerOrder` accepts integer values. It is recommended to use positive numbers for clarity and ease of management.
- **Uniqueness of Values:** It is not mandatory, but recommended, for the values of `headerOrder` to be unique for precise control of the display order.
- **Sorting:** Links in the header are sorted in ascending order of the `headerOrder` value. Links with a lower value are displayed first.

<br/>

### [When to Use](when-to-use)

- **When Setting Up Documentation Header:** To determine the sequence of link display and ensure logical navigation.
- **For Content Prioritization:** When arranging links by importance, providing users with the most sought-after sections first.
- **When Updating Documentation:** To add new links to the header without disrupting the existing order.

<br/>

### [Usage Tips](advice)

- **Incremental Step:** Use a step of 5 or 10 between `headerOrder` values for ease of adding new links.
- **Consider Importance:** Place the most important links at the beginning of the header, assigning them lower `headerOrder` values.
- **Testing:** Check how links are displayed on different devices and screens to ensure the correctness of the order and ease of use.
- **Structure Planning:** Plan in advance which sections or articles should be accessible from the header and determine their order.
- **Consistency:** Adhere to a consistent numbering scheme and naming style.

## [Conclusion](conclusion)

The meta property `headerOrder` is a key tool for managing the order of links displayed in the documentation header.
Proper use of this property allows for creating a logical and intuitive navigation, improving user experience, and facilitating access to important information. Plan the header structure and use `headerOrder` in conjunction with `headerName` for effective interface customization.

<br/>

## [Usage Examples](examples)

### Example 1: Configuring the Order of Links in the Header

**Article 1:**

```md
---
title: Getting Started
displayName: Introduction
order: 1
published: true
headerName: Getting Started
headerOrder: 10
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
headerName: API
headerOrder: 20
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
headerName: Support
headerOrder: 30
---

# Support

If you have any questions, contact our support team...
```

**Result in the documentation header:**

1. Getting Started (headerOrder: 10)
2. API (headerOrder: 20)
3. Support (headerOrder: 30)

<br/>

### Example 2: Omitting the `headerOrder` Value

**Article:**

```md
---
title: Blog
displayName: Blog
order: 4
published: true
headerName: Blog
---

# Blog

Read the latest news and updates...
```

**Result:** Since `headerOrder` is not specified, the link to the "Blog" article will not be displayed in the documentation header.
