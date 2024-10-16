---
id: 29
title: Variables - Markdown Markup
displayName: Variables
order: 5
published: true
historyName: Variables
historyDescription: Using variables in Markdown markup
---

# Using Variables in Markdown

When generating HTML pages from Markdown files, you can use variables to dynamically insert data from the `white-label` JSON.
This allows you to create adaptive content that automatically updates when the source data changes, without the need to edit
the Markdown file itself.

## [Description](description)

**What are variables in Markdown?**

Variables in Markdown are denoted by the construction `{{ var }}`, where `var` is the path to a property in the JSON object. When the page is generated,
these variables are replaced with the corresponding values from the provided JSON object.

**Advantages of using variables:**

- **Dynamic content**: Automatic updating of information on pages when the source data changes.
- **Ease of maintenance**: Changes in data only require updating the JSON object, not multiple files.
- **Flexibility**: Ability to use nested data and complex structures.

**Syntax of variables:**

- **Simple variable**: `{{ variableName }}`
- **Nested properties**: `{{ parent.child.property }}`

**Important to remember:**

- If a variable is not found in the JSON object, it will remain in the text as `{{ var }}`, which may lead to incorrect display.
- It is recommended to check for the presence of all used variables in your JSON object before generating the page.

<br/>

## [Recommendations](recommendations)

- **Data validation**: Before generating pages, check the JSON object for all necessary data.
- **Error handling**: Provide system behavior in case of missing data or errors in the JSON.
- **Documenting variables**: Establish a naming convention for variables and document their usage to facilitate maintenance.

<br/>

## [Conclusion](conclusion)

Using variables in Markdown files allows you to use white-label, resulting in documentation content that remains
independent of a specific company.

<br/>

## [Usage Example](example)

**Step 1: Getting JSON Data**

Let's assume you received the following JSON object from the `white-label` API:

```json
{
  "name": "Example",
  "domain": "https://example-domain.ru",
  "company": {
    "name": "Company Example",
    "domain": "https://company-example-domain.ru",
    "address": {
      "street": "Test Street 1",
      "city": "Moscow",
      "zip": "123456"
    }
  },
  "deep": {
    "company": {
      "name": "Deep Company Example",
      "domain": "https://deep-company-example-domain.ru",
      "contacts": {
        "email": "contact@deep-company-example.ru",
        "phone": "+7 (495) 123-45-67"
      }
    }
  }
}
```

**Step 2: Using Variables in Markdown File**

Let's create a Markdown file `about.md` where we will use variables from the JSON object:

```md
---
title: About {{ company.name }}
displayName: About Company
order: 10
published: true
---

# Welcome to {{ company.name }}

We are pleased to introduce our company - **{{ company.name }}**.

## Basic Information

- **Company Website**: [{{ company.domain }}]({{ company.domain }})
- **Address**:
  - Street: {{ company.address.street }}
  - City: {{ company.address.city }}
  - Zip Code: {{ company.address.zip }}

## Subsidiary Company

We also manage the subsidiary company **{{ deep.company.name }}**.

- **Website**: [{{ deep.company.domain }}]({{ deep.company.domain }})
- **Contacts**:
  - Email: [{{ deep.company.contacts.email }}](mailto:{{ deep.company.contacts.email }})
  - Phone: {{ deep.company.contacts.phone }}

## Business Description

The company **{{ company.name }}** specializes in providing high-quality services in the field of information technology.
We strive for constant development and improvement of our products to meet the needs of our customers.

## Example of Using Variables in Other Elements

- **Company Logo**: ![Logo]({{ company.domain }}/images/logo.png)
- **Job Vacancy Link**: [Join Our Team]({{ company.domain }}/careers)
```

**Step 3: Generating the Page**

When processing a Markdown file with variable substitution from a JSON object, the system will replace all `{{ var }}` constructions with the corresponding values.

**Result:**

After generation, the content of the `about.md` file will look as follows:

```md
---
title: About Company Example
displayName: About Company
order: 10
published: true
---

# Welcome to Company Example

We are pleased to introduce our company - **Company Example**.

## Basic Information

- **Company Website**: [https://company-example-domain.ru](https://company-example-domain.ru)
- **Address**:
  - Street: Example St., 1
  - City: Moscow
  - Postal Code: 123456

## Subsidiary Company

We also manage the subsidiary company **Deep Company Example**.

- **Website**: [https://deep-company-example-domain.ru](https://deep-company-example-domain.ru)
- **Contacts**:
  - Email: [contact@deep-company-example.ru](mailto:contact@deep-company-example.ru)
  - Phone: +7 (495) 123-45-67

## Description of Activities

The company **Company Example** specializes in providing high-quality services in the field of information technology. We strive for constant development and improvement of our products to meet the needs of our clients.

## Example of Using Variables in Other Elements

- **Company Logo**: ![Logo](https://company-example-domain.ru/images/logo.png)
- **Job Vacancy Link**: [Join Our Team](https://company-example-domain.ru/careers)
```

{ /_examples_/ }
