---
id: 11
title: Table of Contents - Documentation Interface
displayName: Table of Contents
order: 60
published: true
historyName: Table of Contents
historyDescription: A navigation list of headings that simplifies searching and accessing sections of the documentation.
---

# Table of Contents

The table of contents of an article is a structured list of headings automatically generated based on the Markdown markup of the document. It is displayed to the right
of the main content of the article and serves as a navigational tool, allowing users to quickly navigate between the article headings. The table of contents
facilitates orientation in the content, especially in long and detailed articles, improving the overall user experience.

![Table of Contents](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-content/refs/heads/main/ru/documentation/markdown/images/table-of-contents.png)

<br/>

## [Key Functions](basic-functions)

- **Content Navigation:** Allows users to instantly jump to the desired sections of the article, reducing the time spent searching for information.
- **Displaying Documentation Structure:** Visualizes the hierarchy of sections and subsections, demonstrating the relationship between different parts of the article.
- **Enhancing Readability:** Divides long articles into logical parts, making the reading and comprehension process easier.
- **User Position Tracking:** Highlights the current section in the table of contents, showing the user's position in the article structure.

<br/>

## [Customization Using Markdown Markup](customization-using-Markdown-markup "Customization with MD Markup")

The table of contents is automatically generated based on headings with links used in the Markdown file. Meta properties on the table of contents have no
effect. To correctly generate the table of contents, certain rules for structuring headings must be followed:

- **Single First-Level Heading (h1):** Each article should have only one h1 heading, which should be located at the beginning of the document. It serves as the main
  heading of the article and is displayed in the table of contents.
- **Proper Hierarchy of Headings:** Use second-level (h2), third-level (h3), and subsequent headings to create subsections and sub-subsections. The nesting of the
  table of contents is determined by the heading level.
- **Absence of h1 Headings After Other Headings:** If an h1 heading appears in the article after other headings, the previous headings will not be included in the
  table of contents.
- **Using Links in Headings:** Headings should contain text links written in Markdown markup to ensure the generation of a table of contents for the article.

### Example of correct heading structure:

```markdown
# Main article heading

## First subsection

### Subsubsection 1.1

## Second subsection

### Subsubsection 2.1
```

<br/>

## [Impact of Heading Structure on Table of Contents](impact-of-heading-structure)

The heading structure directly affects the formation of the table of contents:

- **Heading level:** The higher the heading level (lower number), the deeper it is nested in the table of contents. For example, an h2 heading will be nested under h1, and h3 under h2.
- **Heading position:** The order of appearance of headings in the document determines their order in the table of contents. Headings that appear earlier will be higher in the table of contents list.
- **Uniqueness of h1:** Having only one h1 heading ensures that the table of contents correctly reflects the main topic of the article.

### Incorrect heading structure:

```markdown
## Subsection without main heading

# Main heading after subsections
```

In this case, the table of contents will not consider the "Subsection without main heading" heading, as the main h1 heading is not at the beginning of the document.

<br/>

## [Step-by-Step Setup Guide](step-by-step-setup-guide)

### Step 1: Defining the Article Structure

Before starting to write the article, define its structure and main sections. This will help organize the headings logically and sequentially, ensuring correct formation of the table of contents.

### Step 2: Adding Headings in Markdown

Use headings of different levels to denote main sections and subsections. Start with a heading of the first level.

**Example:**

```markdown
# Licensing Server

## [Task Description](description)

### [Subsystem Requirements](subsystem-requirements)

### [Implementation Requirements](implementation-requirements)

## [High-Level Design](hld "HLD")

### [Application Architecture](application-architecture)

### [Frontend Description](frontent-description)

### [Backend Description](backend-description)

### [Client-Server Interaction Protocol](protocol)
```

### Step 3: Checking the Heading Structure

### Step 5: Navigation Testing

Review the generated article to check the correctness of the table of contents display and navigation convenience.

<br/>

## [Recommendations](recommendations)

- **Maintain a consistent style:** Use the same writing style for headings throughout the article to ensure consistency.
- **Avoid deep nesting levels:** Do not use too many levels of headings to prevent the table of contents from becoming overloaded.
- **Keep headings concise:** Ensure that section titles are short and informative.
- **Check the structure:** Regularly check the structure of headings, especially after making changes to the article.
- **Use links correctly:** Ensure that all links in headings are correct and lead to the corresponding sections.
- **Use abbreviations for contents:** If a link in the table of contents is too long, its display can be different from the heading in the article, the main thing is to convey the meaning of the heading in the article to avoid confusing the user `## [High-Level Design](hld "HLD")`. In the article, it will display as `"High-Level Design"` and in the table of contents as `"HLD"`.

<br/>

## [Usage Examples](examples)

### Example 1: Article with Multiple Levels of Headings

**Markdown Markup:**

```markdown
# Licensing Server

## [Task Description](description)

### [Subsystem Requirements](subsystem-requirements)

### [Implementation Requirements](implementation-requirements)

## [High-Level Design](hld "HLD")

### [Application Architecture](application-architecture)

### [Description of the Client Side](frontent-description)

### [Description of the Server Side](backend-description)

### [Client-Server Interaction Protocol](protocol)
```

**Table of Contents Result:**

- Task Description
  - Subsystem Requirements
  - Implementation Requirements
- HLD
  - Application Architecture
  - Description of the Client Side
  - Description of the Server Side
  - Client-Server Interaction Protocol

### Example 2: Article with h1 Header Not at the Beginning

**Markdown Markup:**

```markdown
## [Task Description](description)

### [Subsystem Requirements](subsystem-requirements)

### [Implementation Requirements](implementation-requirements)

# Licensing Server

## [High-Level Design](hld "HLD")

### [Application Architecture](application-architecture)

### [Description of the Client Side](frontent-description)

### [Description of the Server Side](backend-description)

### [Client-Server Interaction Protocol](protocol)
```

**Table of Contents:**

- HLD
  - Application Architecture
  - Description of the Client Side
  - Description of the Server Side
  - Client-Server Interaction Protocol

Headings "Task Description," "Subsystem Requirements," and "Implementation Requirements" will not be included in the table of contents as the main h1 header is not at the beginning of the document.

<br/>

## [Conclusion](conclusion)

The table of contents of an article is an important tool for organizing and navigating through the article. It provides convenience in finding information, improves user orientation, and contributes to creating a structured and professional appearance of the article. Proper configuration of headings in Markdown markup allows for efficient use of the table of contents, making interaction with documentation more intuitive and user-friendly.

<br/>

## [Additional Resources](additional-resources)

- [Documentation on "Headings"]([18])
