---
id: 28
title: Tables - Markdown Syntax
displayName: Tables
order: 120
published: true
historyName: Tables
historyDescription: Usage in Markdown Syntax
---

# Tables
In this article, we will look at how to create and format tables in Markdown.

<br/>

## Description
Tables in Markdown are created using vertical bar `|`, hyphen `-`, and colon `:` for alignment.
- **Header row**: the first row of the table contains column headers separated by `|`.
- **Divider**: the second row consists of hyphens `-` and defines the boundary between headers and content. Here you can also set column alignment.
- **Data rows**: subsequent rows contain table data, also separated by `|`.

```markdown
| Header 1    | Header 2    | Header 3    |
|-------------|-------------|-------------|
| Cell 1      | Cell 2      | Cell 3      |
| Cell 4      | Cell 5      | Cell 6      |
```

<br/>

## Column Alignment

You can adjust the text alignment in columns using a colon `:` in the divider row.

- **Left-align**:
```markdown
| Header         |
|:-------------- |
| Aligned text   |
```

- **Center-align**:
```markdown
| Header         |
|:--------------:|
| Aligned text   |
```

- **Right-align** (default):
```markdown
| Header         |
|--------------: |
| Aligned text   |
```
<br/>

## Usage Examples

### Simple Table

```markdown
| Name     | Age   | City            |
|--------- |-------|-----------------|
| Ivan     | 25    | Moscow          |
| Maria    | 30    | St. Petersburg  |
| Alexei   | 28    | Novosibirsk     |
```
#### Result

| Name     | Age   | City            |
|--------- |-------|-----------------|
| Ivan     | 25    | Moscow          |
| Maria    | 30    | St. Petersburg  |
| Alexei   | 28    | Novosibirsk     |

<br/>

### Table with Alignment

```markdown
| Product    | Price (rub) | Quantity |
|:---------- |-----------: |--------: |
| Apples     |     100.50  |      10  |
| Bananas    |      80.00  |       5  |
| Oranges    |     120.75  |       8  |
```

#### Result

| Product     | Price (rub) | Quantity |
|:------------|------------:|---------:|
| Apples      |      100.50 |       10 |
| Bananas     |       80.00 |        5 |
| Oranges     |      120.75 |        8 |

<br/>

### Table with different alignment

```markdown
| Element     | Description             |   Price (rub) |
|:------------|:-----------------------:|-------------:|
| Laptop      | Powerful gaming laptop  |     50000.00 |
| Smartphone  | Latest model            |     30000.00 |
| Headphones  | Wireless headphones      |      5000.00 |
```
#### Result

| Element     |         Description       |   Price (rub) |
|:------------|:-----------------------:|-------------:|
| Laptop      |  Powerful gaming laptop  |     50000.00 |
| Smartphone  |     Latest model         |     30000.00 |
| Headphones  |  Wireless headphones      |      5000.00 |
