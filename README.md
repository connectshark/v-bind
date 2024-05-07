# v-bind
[![build status](https://github.com/connectshark/v-bind/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/connectshark/v-bind/actions/workflows/deploy.yml)
[![create-release](https://github.com/connectshark/v-bind/actions/workflows/create-release.yml/badge.svg?branch=main)](https://github.com/connectshark/v-bind/actions/workflows/create-release.yml)
[![GitHub last commit](https://img.shields.io/github/last-commit/connectshark/v-bind.svg?style=flat)](https://github.com/connectshark/v-bind)
![GitHub stars](https://img.shields.io/github/stars/connectshark/v-bind.svg?style=social&label=Stars&style=plastic)


![https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)
![https://img.shields.io/badge/tailwindcss-35495E?style=for-the-badge&logo=tailwindcss&logoColor=38BCF8](https://img.shields.io/badge/tailwindcss-35495E?style=for-the-badge&logo=tailwindcss&logoColor=38BCF8)


## 目錄

- [截圖](#截圖)
- [專案目的](#專案目的)
- [版權](#版權)

## 截圖

![](/readme/cover.png)

## 專案目的

使用`v-bind`替換原本使用`props`的習慣。

父層資料傳遞到元件中，原本是物件型態的資料不用在父層解構，直接使用`v-bind`綁定資料，就可以直接在元件中提取物件的屬性使用。

```js
// 原始資料

const list = [
  {
    "id": 1,
    "name": "John Doe",
    "occupation": "Software Engineer",
    "company": "ABC Tech",
    "email": "john.doe@example.com",
    "phone": "+1 (555) 123-4567",
    "address": {
      "street": "123 Main St",
      "city": "Anytown",
      "state": "CA",
      "zip": "12345",
      "country": "USA"
    }
  },
  ...
]
```


```html
// index.vue
<tbody>
  <tr class=" bg-indigo-100 odd:bg-indigo-50" v-for="item in list">
    <Card v-bind="item" />
  </tr>
</tbody>
```

```html
// Card.vue
<template>
  <td>{{ name }}</td>
  <td>{{ occupation }}</td>
  <td>{{ email }}</td>
</template>

<script setup>
defineProps({
  name: String,
  occupation: String,
  email: String
})
</script>
```

## 版權

[MIT](/LICENSE).