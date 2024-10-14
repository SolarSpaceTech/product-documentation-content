---
id: 36
title: Brief description - Meta properties
displayName: Description
order: 1
published: true
historyName: List of meta properties
historyDescription: Provides a brief description of Meta properties
---

# Description

Meta properties are a key tool for generating HTML pages based on a file structure consisting of Markdown files.
They are used to manage various aspects of displaying and organizing documentation content.

<br/>

| Property              | Description                                                                                                                                    | Data type and possible values                                                     | Required | Implemented |
| :-------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------- | :------: | :---------: |
| `id`                  | Unique identifier of the article within the language; used for short links and visit history                                                   | Number                                                                            |    +     |      -      |
| `title`               | Article title displayed in the browser tab                                                                                                     | String                                                                            |    +     |      +      |
| `displayName`         | Article title in the menu and breadcrumbs                                                                                                      | String                                                                            |    +     |      +      |
| `order`               | Defines the order of the article in the menu within the current section                                                                        | Number                                                                            |    +     |      +      |
| `published`           | Determines whether the article will be generated and whether it should be displayed in interface elements                                      | Boolean value (`true` or `false`)                                                 |    +     |      +      |
| `historyName`         | Article title in the visit history block                                                                                                       | String                                                                            |    +     |      -      |
| `historyDescription`  | Brief description of the article in the visit history block                                                                                    | String                                                                            |    +     |      -      |
| `categories`          | List of categories to which articles may belong; used to determine sections on the main page                                                   | List of strings (e.g., `Getting Started`, `Services`, `Resource Settings`, `FAQ`) |    -     |      -      |
| `category`            | Name of the section on the main page where the article will be placed; must match one of the values in `categories` from the language metadata | String                                                                            |    -     |      -      |
| `categoryName`        | Article title in the section on the main page                                                                                                  | String                                                                            |    -     |      -      |
| `categoryDescription` | Brief description of the article in the section on the main page                                                                               | String                                                                            |    -     |      -      |
| `categoryOrder`       | Order of the article within the section on the main page                                                                                       | Number                                                                            |    -     |      -      |
| `categoryIcon`        | URL of the icon displayed next to the article in the section on the main page                                                                  | String (URL)                                                                      |    -     |      -      |
| `headerName`          | Name of the link to the article in the site header                                                                                             | String                                                                            |    -     |      -      |
| `headerOrder`         | Display order of the link in the site header                                                                                                   | Number                                                                            |    -     |      -      |
| `footerName`          | Name of the link to the article in the site footer                                                                                             | String                                                                            |    -     |      -      |
| `footerOrder`         | Display order of the link in the site footer                                                                                                   | Number                                                                            |    -     |      -      |

**Column Legend:**

- **Property**: The name of the meta property of the article.
- **Description**: A brief description of the purpose of the property.
- **Data Type and Possible Values**: Expected data type and allowable values.
- **Mandatory**: The necessity of using the meta property.
- **Implemented**: The current implementation status of the property.
