---
id: 44
title: Description of id - General - Meta properties
displayName: id
order: 10
published: true
historyName: Description of meta property id
historyDescription: Unique identifier of an article used for short links and visit history in the application.
---


# Property id

**Meta property:** `id`

**Data type:** Number

<br/>

## [Description](description)

The `id` property is a unique identifier of an article within a specific language in the documentation. It plays a key role in organizing content,
providing the ability to create short links and track the visit history of articles by users.

<br/>

### [Main functions](basic-functions)

- **Unique identification**: Ensures that each article has its own unique number, preventing confusion and collisions.
- **Short links**: Allows for creating short and easy-to-remember links to articles using their id.
- **Visit history**: Enables tracking and recording the visit history of articles by users, enhancing the user experience.

<br/>

### [How it works with other meta properties](with-other-properties)

- **Connection with visit history**: The `id` property is used in conjunction with `historyName` and `historyDescription` to form records in the visit history block.
- **Link formation**: When creating links within content, you can use the syntax [Link text]([id]), where id is replaced with the numerical identifier
of the article. This simplifies navigation and maintains links when URL structure changes.
- **Multilingual support**: Since the id is unique within a language, this allows for having corresponding articles in different languages with the same `id`, facilitating
localization and switching between language versions.

<br/>

### [Important notes](notes)

- **Uniqueness**: Ensure that the `id` is unique for each article within a language. Repeating identifiers can lead to incorrect
functioning of links and visit history.
- **Sequence**: It is recommended to adhere to a consistent system of assigning `id` (e.g., incrementally or based on a specific logic),
to facilitate content management.
- **Immutability**: After assigning an `id`, it is strongly recommended not to change it, as this may disrupt existing links and visit history.


<br/>

### [When to Use](when-to-use)

- **Navigation**: To create internal links between articles using short links based on `id`.
- **Localization**: When creating multilingual applications, where articles in different languages have corresponding `id`.

<br/>

### [Usage Tips](advice)

- **Documentation**: Keep track of assigned `id` and their corresponding articles.
- **Updating Links**: When changing the article id (which is highly not recommended), make sure to update all links that reference it.
- **Deleting an Article**: When deleting an article, it is recommended not to reuse the freed id.

<br/>

## [Conclusion](conclusion)

The `id` property is a fundamental meta property for organizing and managing content in documentation. Proper use of `id` simplifies navigation, enhances user experience, and contributes to the maintainability of the system.

<br/>

## [Usage Examples](examples)

### Example 1: Creating a Short Link to an Article

Article file: `ru/documentation/guide.md`

```markdown
---
id: 42
title: User Guide
displayName: Guide
published: true
historyName: Guide
historyDescription: Description of the user guide
---
# User Guide

Welcome to the user guide.
```

Article file: `ru/documentation/new-guide.md`

```markdown
---
id: 43
title: New User Guide
displayName: New Guide
published: true
historyName: New Guide
historyDescription: Description of the new user guide
---
# New User Guide

Welcome to the new user guide.

Using a short link in another article:

To access the old version of the guide, see [Guide]([42]).
```

Description:

- When rendered, `[42]` will be converted to the link `/ru/documentation/guide`, resulting in `[Guide](/ru/documentation/guide)`.
- If the path or filename `guide.md` changes, the link will remain correct as it is based on the `id`.

<br/>

### Example 2: Tracking Visit History

- When visiting the article with `id: 42`, information about it is added to the visit history block, and the display is formed based on `historyName` and `historyDescription`.
- This allows the user to easily return to recently viewed articles.
