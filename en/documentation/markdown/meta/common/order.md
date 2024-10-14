---
id: 45
title: Description of order - General - Meta properties
displayName: order
order: 40
published: true
historyName: Description of the meta property order
historyDescription: The meta property order defines the order of displaying sections and articles in the documentation menu for easy navigation.
---

# Property order

**Meta property:** `order`

**Data type:** Number

**Scope of influence:**
![Property influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/order.png)

<br/>

## [Description](description)

The meta property `order` is used to define the order of displaying sections and articles in the documentation menu, as well as within sections.
This property allows organizing the documentation structure in a logical sequence, providing convenient navigation for users.

<br/>

### [Main functions](basic-functions)

- **Menu order management:** Defines the sequence in which sections and articles are displayed in the site menu.
- **Ordering within sections:** Affects the order of articles within the current section, allowing materials to be presented from main to additional.
- **Study sequence:** Helps establish a logical reading order, guiding users through the documentation step by step.

<br/>

### [How it works with other meta properties](with-other-properties)

- **For sections:**

  - **`displayName`:** Section name in the menu and breadcrumbs.
  - **`published`:** If set to `false`, the section and its content are not displayed in the menu, regardless of the `order` value.

- **For articles:**
  - **`displayName`:** Article name in the menu and breadcrumbs.
  - **`published`:** If set to `false`, the article is not displayed in the menu and other navigation elements, regardless of the `order` value.

<br/>

### [Important notes](notes)

- **Mandatory:** The meta property `order` is mandatory, its use is necessary for precise control of the order of elements.
- **Value range:** Accepts integer values. Positive numbers are usually used for ease of management.
- **Uniqueness:** The `order` values do not necessarily have to be unique, but it helps to avoid uncertainty in the display order.
- **Sorting:** Elements are sorted in ascending order of the `order` value. Elements with a lower value are displayed above.

<br/>

### [When to Use](when-to-use)

- **Always for controlling display order:** It is important that sections and articles are displayed in a specific logical sequence.
- **When expanding documentation:** Allows adding new materials in the right place without disrupting the existing structure.
- **For improving user experience:** Helps users easily navigate and find the necessary information.

<br/>

### [Usage Tips](advice)

- **Incremental step:** Use a step of 10 or 5 between values to easily add new elements.
- **Structure planning:** Plan the logical sequence of sections and articles in advance.
- **Consistent numbering:** Stick to one numbering scheme throughout the documentation.
- **Grouping:** If necessary, group related materials using close `order` values.
- **Documentation:** Keep track of `order` values for large projects to avoid conflicts.

<br/>

## [Conclusion](conclusion)

The `order` meta property is a key tool for managing the display order of sections and articles in documentation.
It allows creating a logical and understandable structure, facilitating navigation and enhancing the user experience when working with documentation.

<br/>

## [Usage Examples](examples)

### Example 1: Ordering sections in the menu

**`metadata.md` file for the "Introduction" section:**

```md
---
displayName: Introduction
order: 1
published: true
---
```

**`metadata.md` file for the "Guides" section:**

```md
---
displayName: Guides
order: 2
published: true
---
```

**`metadata.md` file for the "API Reference" section:**

```md
---
displayName: API Reference
order: 3
published: true
---
```

**Result in the menu:**

1. Introduction
2. Guides
3. API Reference

<br/>

### Example 2: Ordering articles within a section

**Articles in the "Guides" section:**

- **`installation.md`:**

  ```md
  ---
  title: Product Installation
  displayName: Installation
  order: 1
  published: true
  ---

  # Product Installation
  ```

- **`configuration.md`:**

  ```md
  ---
  title: Product Configuration
  displayName: Configuration
  order: 2
  published: true
  ---

  # Product Configuration
  ```

- **`usage.md`:**

  ```md
  ---
  title: Product Usage
  displayName: Usage
  order: 3
  published: true
  ---

  # Product Usage
  ```

**Result in the menu inside the "Guides" section:**

1. Installation
2. Configuration
3. Usage

```

```
