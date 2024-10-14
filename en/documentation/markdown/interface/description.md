---
id: 5
title: Description - Documentation Interface
displayName: Description
order: 1
published: true
historyName: Description
historyDescription: Brief description of interface elements.
headerName: Description
headerOrder: 3
footerName: Description
footerOrder: 3
category: Resource Configuration
categoryName: Description
categoryDescription: Brief description of interface elements.
categoryOrder: 3
categoryIcon: https://img.solarspace.pro/docs/desktop.svg
---

# Description of Documentation Elements

Meta properties allow flexible control over the display of various documentation elements. With them, you can configure the following elements:

- **[Home Page]([9])**

  - **`category`**: Defines the section of the home page to display the article (`start`, `services`, `useful`, `faq`).
  - **`categoryName`**: Sets the article name in the section on the home page.
  - **`categoryDescription`**: Provides a brief description of the article in the section.
  - **`categoryOrder`**: Determines the order of displaying articles within the section.
  - **`categoryIcon`**: Specifies the icon for the article in the section.

- **[Header]([7])**

  - **`headerName`**: Sets the name of the link to the article in the header.
  - **`headerOrder`**: Determines the order of displaying links in the header.

- **[Footer]([6])**

  - **`footerName`**: Sets the name of the link to the article in the footer.
  - **`footerOrder`**: Determines the order of displaying links in the footer.

- **[Menu]([10])**

  - **`displayName`**: Sets the name of sections and articles in the menu.
  - **`order`**: Determines the order of displaying sections and articles in the menu.

- **[Breadcrumbs]([4])**

  - **`displayName`**: Sets the name of sections and articles in the breadcrumbs.

- **[Article Table of Contents]([11])**

- **[Visit History]([8])**

  - **`historyName`**: Sets the name of the article in the visit history.
  - **`historyDescription`**: Provides a brief description of the article in the visit history.

- **Content Visibility**

- **`published`**: Controls the visibility of sections and articles on the site. If set to `false`, the element is not displayed in the menu, header, footer,
  on the home page, and visit history.

- **Page Title**
  - **`title`**: Defines the text displayed in the browser tab title.

By using these meta properties, you can customize the documentation interface, providing convenient navigation and access to important sections for users.
