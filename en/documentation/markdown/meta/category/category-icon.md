---
id: 33
title: Description of categoryIcon - Main Sections - Meta Properties
displayName: categoryIcon
order: 110
published: true
historyName: Description of the meta property categoryIcon
historyDescription: The meta property categoryIcon adds an icon to the article on the main page, improving visual perception and navigation.
---

# Property categoryIcon

**Meta property:** `categoryIcon`

**Data type:** String (URL or path to an image)

**Scope of influence:**
![Property Influence](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/category-icon.png)


<br/>

## [Description](description)

The meta property `categoryIcon` is used to specify an icon that will be displayed next to the article title in a specific section on the main page of the site. This property allows visually highlighting articles, making them more attractive and recognizable to users.

<br/>

### [Basic Functions](basic-functions)

- **Visual design:** Adds an icon to the article in a section on the main page, improving the visual perception of the content.
- **Enhanced navigation:** Helps users find the desired articles faster through associative images.
- **Branding:** Allows the use of branded icons or symbols that correspond to the theme of the article or the company's style.

<br/>

### [How It Works with Other Meta Properties](with-other-properties)

- **`category`:** Determines the section on the main page where the article will be displayed. `categoryIcon` is applied to articles in these sections.
- **`categoryName`:** The title of the article displayed in the section on the main page. The icon will be displayed next to this title.
- **`categoryDescription`:** A brief description of the article in the section.
- **`categoryOrder`:** Determines the order of displaying the article within the section.

<br/>

### [Important Notes](notes)

- **Value format:** `categoryIcon` should contain a string with a URL or a relative path to the icon image (e.g., `/icons/my-icon.svg`).
- **Supported image formats:** Typically, supported formats include SVG, PNG, JPG, and other web-compatible formats.
- **Icon size:** It is recommended to use icons of optimal size for correct display and page loading speed.


<br/>

### [When to Use](when-to-use)

- **Visual Identification:** When you want articles to be easily recognizable by an icon.
- **Attention Grabbing:** To draw users' attention to specific articles in a section.
- **Content Branding:** When using branded icons that match the company's style or the article's theme.

<br/>

### [Usage Tips](advice)

- **Semantics:** Choose icons that are logically related to the content of the article.
- **Simplicity:** Use simple and clear icons so that users immediately understand their meaning.
- **Color Palette:** Icons should match the overall color scheme of the site.
- **Image Quality:** Use high-quality icons with optimized file size for fast page loading.
- **Consistent Style:** Maintain a consistent style of icons throughout the documentation.
- **Accessibility:** Ensure that icons are understandable and distinguishable for all users.

<br/>

## [Conclusion](conclusion)

The `categoryIcon` meta property is a useful tool for enhancing the visual representation of articles on the documentation homepage.
It allows adding icons to articles in sections, which can increase user engagement and improve navigation.
Proper use of icons makes the interface more intuitive and appealing.

<br/>

## [Usage Examples](examples)

### Example 1: Adding an Icon to an Article in the `services` Section

```md
---
title: Cloud Solutions
displayName: Cloud
order: 2
published: true
category: services
categoryName: Cloud Solutions
categoryDescription: Secure and scalable cloud services
categoryOrder: 10
categoryIcon: /icons/cloud.svg
---
# Cloud Solutions

We offer a wide range of cloud services for your business...
```

In this example, **`categoryIcon`:** Specifies the path to the icon `/icons/cloud.svg`, which will be displayed next to the title "Cloud Solutions" in the `services` section on the homepage.

<br/>

### Example 2: Article Without an Icon

```md
---
title: Contact Information
displayName: Contacts
order: 5
published: true
category: useful
categoryName: Contact Us
categoryDescription: We are always ready to help you
categoryOrder: 20
---
# Contact Information

You can contact us through the following channels...
```

In this example **`categoryIcon`:** property is not specified, so the icon next to the article title in the `useful` section will not be displayed.
