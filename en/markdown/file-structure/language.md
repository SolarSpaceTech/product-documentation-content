---
id: 2
title: New Language - File Structure
displayName: New Language
order: 10
published: true
historyName: Adding a New Language
historyDescription: Detailed explanation of adding a new language to the site, maintaining the structure, and correctly translating the content.
---

# Adding a New Language

In this guide, we will detail the process of adding a new language to the file structure so that the content is automatically displayed in the desired language and seamlessly integrated into all elements of the user interface.

<br/>

## [Language Directory Structure](structure)

### Root Directory

- **Project Root**: Contains subdirectories for each supported language.
- **Directory Naming**: Each language directory should be named according to the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard (e.g., `ru` for Russian, `en` for English, `fr` for French).

### Unified File Structure

- **Consistency**: All language directories should have the **same file structure**.
- **Articles and Sections**: File names of articles and sections, as well as their identifiers (`id`), should match across all language versions.

<br/>

## [Adding a New Language Process](process)

### Step 1: Create a Language Directory

**Create a new directory** in the project root with the name of the new language following the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard.
Example for French language: `/fr`

### Step 2: Copy File Structure

- **Copy** the complete file structure from an existing language directory (e.g., `/en` or `/ru`) to the new directory `/fr`, **including** all files and subdirectories.
- **Note**: Ensure to copy not only article files but also all `metadata.md` files of sections.

### Step 3: Update Metadata

- **Language Section `metadata.md` file**:
  - Specify the language name in the `displayName` field, which will be displayed when selecting the language.
  - Specify the `categories` field, which will contain a list of sections on the homepage, for the new language.
- **`metadata.md` files**:
  - In each section, update the `displayName` field to the corresponding translation.
  - Check the `published` field to ensure sections are displayed correctly.
- **Article Files**:
  - Update article metadata, translating fields such as `title`, `displayName`, `historyName`, `historyDescription`, `categoryName`, `categoryDescription`, `headerName`, `footerName`.

### Step 4: Translate the Content

- **Translate the content** of each article in the `.md` files to the new language.
  - **Headings and Text**: Translate all headings, subheadings, and main text.
  - **Variables**: Leave `{{ var }}` constructs unchanged, they will be automatically replaced with the corresponding values.

### Step 5: Save Unique Identifiers

- **`id` Identifiers**:
  - Ensure that the `id` field in the metadata of each article matches the corresponding articles in other language directories.
  - **Important**: This is necessary for the correct functioning of short links and visit history.

### Step 6: Check Links and Paths

- **Article Paths**:

  - Verify that URL paths are correctly formed based on the new language directory.
  - Example: The article `/fr/documentation/start.md` will be accessible at `/fr/documentation/start`.

- **Short Links**:
  - Ensure that short links using `[id]` work correctly and point to the corresponding articles in the new language.

### Step 7: Update Icons and Resources (Optional)

- If language-specific icons or resources are used, update the paths in the metadata, for example, `categoryIcon`.

### Step 8: Testing

- **Check Display**:
  - Site Menu: Ensure that all sections and articles are displayed correctly.
  - Homepage: Verify the display of articles in the respective sections.
  - Header and Footer: Ensure that links are displayed with correct names and in the right order.
- **Navigation**:
  - Go through all links and make sure they lead to the correct pages.

<br/>

## [Important Notes](notes)

- **Data Consistency**: It is important that the directory structure, file names, and `id` identifiers are **completely identical** across language versions.
- **Variables**: Using `{{ var }}` variables facilitates multilingual support, as they automatically substitute the necessary values from `white-label`.

<br/>

## [Conclusion](conclusion)

Adding a new language involves creating a language directory, copying the file structure, translating content and metadata, and thorough testing to ensure correct display on the site.
