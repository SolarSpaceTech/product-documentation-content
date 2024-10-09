---
id: 15
title: Блочный код - Markdown-разметка
displayName: Блочный код
order: 100
published: true
historyName: Блочный код
historyDescription: Использование в Markdown-разметки
---

# Блочный код
В данном разделе приведён пример использования блочного кода.

<br/>

## Описание

<p>
  Для использования блочного кода код оборачивают в <code class="code-inline">```</code>
</p>

<br/>

## Пример использования

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

## Результат

```typescript
  import { Injectable } from '@angular/core';
  import { Token } from 'marked';
  import { MarkdownRendererModel } from 'markdown/models/markdown-renderer.model';
  import { MarkdownHtmlElementBuilderService } from './markdown-html-element-builder.service';
  import { MarkdownOtherElementBuilderService } from './markdown-other-element-builder.service';
  import { MarkdownComponentBuilderService } from './markdown-component-builder.service';
```
