---
id: 15
title: Block Code - Markdown Markup
displayName: Block Code
order: 100
published: true
historyName: Block Code
historyDescription: Usage in Markdown Markup
---

# Block Code
This section provides an example of using block code.

<br/>

## Description

<p>
  To use block code, wrap the code in <code class="code-inline">```</code>
</p>

<br/>

## Example Usage

<code class="block-code">
```typescript
  import { Injectable } from '@angular/core';
  import { Token } from 'marked';
  import { MarkdownRendererModel } from 'markdown/models/markdown-renderer.model';
  import { MarkdownHtmlElementBuilderService } from './markdown-html-element-builder.service';
  import { MarkdownOtherElementBuilderService } from './markdown-other-element-builder.service';
  import { MarkdownComponentBuilderService } from './markdown-component-builder.service';
```
</code>

<br/>

## Result

```typescript
  import { Injectable } from '@angular/core';
  import { Token } from 'marked';
  import { MarkdownRendererModel } from 'markdown/models/markdown-renderer.model';
  import { MarkdownHtmlElementBuilderService } from './markdown-html-element-builder.service';
  import { MarkdownOtherElementBuilderService } from './markdown-other-element-builder.service';
  import { MarkdownComponentBuilderService } from './markdown-component-builder.service';
```
