---
id: 3
title: Creating Sections - File Structure
displayName: Creating Sections
order: 10
published: true
historyName: Creating Sections
historyDescription: Detailed description of the process of creating sections, configuring them through metadata.md, and their impact on the documentation interface.
---

# Creating Sections

Creating sections is an important step in organizing documentation. Sections help structure information, making it more accessible and understandable for users. In this guide, we will examine in detail the process of creating sections, configuring them using metadata, and their impact on various elements of the user interface.

<br/>

## [Section Structure](structure)

### Directories as Sections

- **Each directory** in the file system represents a separate section of the site.
- **Nested directories** allow you to create a hierarchical structure of sections and subsections.

### `metadata.md` Files

- **Section Description**: Each section should have a `metadata.md` file containing the section's metadata.
- **Metadata Format**: Metadata is specified between triple dashes `---`.

<br/>

## [Section Metadata](metadata)

Section metadata defines their display and behavior on the site.

### `metadata.md` Structure

Example structure of the `metadata.md` file for a section:

```md
---
displayName: Section Name
order: Order Number
published: true or false
---
```

### Description of Metadata Fields

- **displayName**: The name of the section displayed in the menu and breadcrumbs.
- **order**: The display order of the section in the menu relative to other sections at the same level.
- **published**: Indicates whether the section should be displayed on the site. If `false` or absent, the section is not displayed.

<br/>

## [Section Creation Process](process)

### Step 1: Create a Directory

- **Create a new directory** in the desired location of the file structure, representing a new section.
  - Example: `documentation/new-section`

### Step 2: Add the `metadata.md` File

- **Create the `metadata.md` file** inside the new directory.
- **Fill in the metadata** according to your requirements.

```md
---
displayName: New Section
order: 50
published: true
---
```

### Step 3: Add Articles (Optional)

- **Add article files** with the `.md` extension to the section directory.
- **Configure article metadata** according to the requirements.

### Step 4: Creating Nested Sections (Optional)

- **Create subdirectories** within the section to create nested sections.
- **Add `metadata.md`** to each subdirectory with the corresponding metadata.

<br/>

## [Impact of Sections on User Interface](impact)

### Site Menu

- **Displaying Sections**: The menu is built based on the file structure and section metadata.
- **Influence Fields**:
  - `displayName`: Defines the section name in the menu.
  - `order`: Determines the display order of sections.
  - `published`: If `false` or absent, the section is not displayed.

### Breadcrumbs

- **Path Formation**: Breadcrumbs display the path from the root section to the current article.
- **Using `displayName`**: Section and article names are taken from the `displayName` field.

### Homepage and Other Elements

- **Indirect Influence**: Sections impact content organization, which is reflected in other interface elements.

<br/>

## [Practical Example of Section Creation](example)

### Step 1: Creating the "Examples" Section

- **Directory**: `documentation/examples`
- **`metadata.md` File**:

```md
---
displayName: Examples
order: 20
published: true
---
```

### Step 2: Adding an Article to the Section

- **Article File**: `documentation/examples/sample.md`
- **Article Metadata**:

```md
---
id: 100
title: Example Article
displayName: Example Article
order: 10
published: true
---
```

### Step 3: Display Verification

- **Site Menu**: The "Examples" section appears in the menu with an order number of 20.
- **Breadcrumbs**: When viewing the "Example Article" article, breadcrumbs will display the path:
  "Documentation > Examples > Example Article".

<br/>

## [Important Notes](notes)

- **Uniqueness of `order`**: Ensure sequential numbers to avoid conflicts in display.
- **`published` Field**: Control the visibility of sections and articles using this field.
- **Consistency**: Ensure that the file system structure reflects logical content organization.

<br/>

## [Conclusion](conclusion)

Creating sections allows for efficient documentation organization and improves navigation.

```

```
