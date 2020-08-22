---
title: Client Libraries
description: ""
position: 4
category: Guide
---

The available libraries for client-side apps:

- Vuejs: [Vue-Contenu](https://npmjs.com/vue-contenu)

Very soon, more libraries will get ready for other front-end javascript frameworks. Contributing is wholeheartedly accepted ❤️.

### Installation

<code-group>
  <code-block label="Vue" active>

```bash
$ yarn add vue-contenu
```

  </code-block>
</code-group>

### Add to project

<code-group>
  <code-block label="Vue" active>

```js
// main.js
import Vue from "vue";
import Contenu from "vue-contenu";
Vue.use(Contenu, {
  serverAddress: "http://localhost:8080",
});
```

  </code-block>
</code-group>

### Usage

<code-group>
  <code-block label="Vue" active>

```vue
<template>
  <div>
    <p>{{ this.$contenu.header.name.parse() }}</p>
    <p>{{ this.$contenu.header.job.parse() }}</p>
  </div>
</template>
```

  </code-block>
</code-group>
<alert type="warning">

The `parse()` function should be called after each object you want to access.

</alert>
This object would be like

```js
header :{
  name: "",
  jon: ""
}
```
