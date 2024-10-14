---
id: 46
title: Description of published - General - Meta properties
displayName: published
order: 50
published: true
historyName: Description of the meta property published
historyDescription: The meta property published controls the visibility of an article or section in the menu, header, and on the main documentation page.
---

# Property published

**Meta property:** `published`

**Data type:** Boolean value

**Possible values:** `true` or `false`

<br/>

## [Description](description)

The meta property `published` is used to control the visibility of sections and articles in the generated documentation. It determines whether the corresponding
sections or articles will be displayed in various elements of the user interface, such as the menu, header, footer, and main page.

<br/>

### [Basic Functions](basic-functions)

- **Menu display control:** If `published` is set to `true`, the section or article is displayed in the menu. If `false` or the property is missing, the element is not displayed.
- **Visibility control in header and footer:** For articles, `published` affects the display of links in the site header and footer.
- **Exclusion from the main page:** Articles with `published: false` are not displayed in sections on the main page, even if `category` and related properties are specified.
- **Hiding from users:** Allows hiding certain sections or articles from users without deleting them from the file structure.

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **With `displayName`:** If `published: false`, the value of `displayName` is not displayed in the menu and breadcrumbs.
- **With `headerName` and `headerOrder`:** Even if these properties are specified, the article will not appear in the header if `published: false`.
- **With `footerName` and `footerOrder`:** Similarly, the article will not be displayed in the footer when `published: false`.
- **With `category` and related properties:** Articles with `published: false` will not be displayed in the corresponding sections on the main page.
- **With nested elements:** If a section has `published: false`, all its nested sections and articles will also not be displayed, regardless of their own `published` properties.


<br/>

### [Important Notes](notes)

- **By default:** If the `published` property is missing, it is assumed to be `false`, and the element will not be displayed.
- **Navigation Impact:** Elements with `published: false` do not appear in the menu, header, footer, and homepage, but can be accessed through a direct link.

<br/>

### [When to Use](when-to-use)

- **During Development:** When creating new sections or articles that are not yet ready for public access.
- **For Unpublishing:** When you need to temporarily or permanently hide content from users.
- **For Internal Documents:** If there are articles or sections intended only for internal use and should not be visible to users.

<br/>

### [Usage Tips](advice)

- **Content Management:** Use `published: false` to manage the visibility of materials without deleting them.
- **Workflow:** Include `published: false` as part of the process of creating and reviewing new materials.
- **Consistency:** Ensure consistent use of `published` throughout the documentation to simplify content management.
- **Explicit Specification:** It is recommended to always explicitly specify `published: true` or `published: false` for clarity.
- **Nested Checking:** Remember that `published: false` for a section hides all nested elements, regardless of their own settings.
- **Status Update:** Don't forget to change the value of `published` to `true` when the material is ready for publication.


## [Conclusion](conclusion)

The `published` meta property is a key tool for controlling the visibility of sections and articles in the documentation. It allows flexible content management,
ensuring that users are presented with only relevant and ready-to-use information. Proper use of `published` enhances the quality of documentation.

<br/>

## [Usage Examples](examples)

### Example 1: Hiding a Section from the Menu

**`metadata.md` file for the section:**

```md
---
displayName: Drafts
order: 99
published: false
---
```

- **Result:** The "Drafts" section and all its content will not be displayed in the menu and navigation.

### Example 2: Hiding an article from all interface elements

**Article `upcoming-features.md`:**

```md
---
title: Future Features
displayName: Future Features
order: 10
published: false
category: start
categoryName: Coming in version 2.0
categoryDescription: Preview of new features
categoryOrder: 1
categoryIcon: /icons/coming-soon.svg
headerName: Future Features
headerOrder: 50
footerName: Future Features
footerOrder: 50
---
# Future Features

*This article is under development and will be published soon.*
```

- **Result:** The "Future Features" article will not be displayed in the menu, header, footer, or on the homepage.

---
