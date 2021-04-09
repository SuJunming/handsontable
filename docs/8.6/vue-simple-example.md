---
title: Basic example
permalink: /8.6/vue-simple-example
canonicalUrl: /vue-simple-example
---

# {{ $frontmatter.title }}

A simple implementation of the `@handsontable/vue` component.

A `div` element of `id="example"` where the `@handsontable/vue` component will be rendered. HTML file:

```html
<hot-table :settings="hotSettings"></hot-table>
```

An implementation of the `@handsontable/vue` component. JS file:

```js
import Vue from 'vue';
import { HotTable } from '@handsontable/vue';
import Handsontable from 'handsontable';

new Vue({
  el: '#example1',
  data: function() {
    return {
      hotSettings: {
        data: Handsontable.helper.createSpreadsheetData(6, 10),
        colHeaders: true
      }
    }
  },
  components: {
    HotTable
  }
});
```