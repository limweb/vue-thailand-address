# Vue Thailand Address 🇹🇭
[![license](https://img.shields.io/github/license/gluons/vue-thailand-address.svg?style=flat-square)](./LICENSE)
[![vue 2](https://img.shields.io/badge/vue-2-42b983.svg?style=flat-square)](https://vuejs.org)
[![npm](https://img.shields.io/npm/v/vue-thailand-address.svg?style=flat-square)](https://www.npmjs.com/package/vue-thailand-address)
[![npm](https://img.shields.io/npm/dt/vue-thailand-address.svg?style=flat-square)](https://www.npmjs.com/package/vue-thailand-address)
[![Dependency Status](https://dependencyci.com/github/gluons/vue-thailand-address/badge?style=flat-square)](https://dependencyci.com/github/gluons/vue-thailand-address)
[![ESLint Gluons](https://img.shields.io/badge/code%20style-gluons-9C27B0.svg?style=flat-square)](https://github.com/gluons/eslint-config-gluons)
[![Gitmoji](https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67.svg?style=flat-square)](https://github.com/carloscuesta/gitmoji)

ตัวช่วยกรอกที่อยู่ของไทย สำหรับ [Vue](https://vuejs.org) (ปราศจาก jQuery 🎉)

## 🔥 ต้นกำเนิด

มาจาก [jquery.Thailand.js](https://github.com/earthchie/jquery.Thailand.js) ของ [@earthchie](https://github.com/earthchie)

## ⚙️ การติดตั้ง

**ด้วย [NPM](https://www.npmjs.com/):**

```bash
npm install vue-thailand-address
```

**ด้วย [Yarn](https://yarnpkg.com/):**

```bash
yarn add vue-thailand-address
```

## 🛂 วิธีใช้

```javascript
import Vue from 'vue';
import VueThailandAddress from 'vue-thailand-address';

// เพิ่ม stylesheet ของ Vue Thailand Address เข้าไป
import 'vue-thailand-address/dist/vue-thailand-address.css';

// ใช้ Plugin
Vue.use(VueGitHubCorners);
```

```vue
<template>
	<div id="app">
		<address-form></address-form>
	</div>
</template>
```

## 🗂 ชนิดของไฟล์ในโฟลเดอร์ `dist`

- `vue-thailand-address.css` (Unminified) และ `vue-thailand-address.min.css` (Minified): ไฟล์ stylesheet
- `db.json`: ไฟล์ฐานข้อมูล (นำมาจาก [earthchie/jquery.Thailand.js's `db.json`](https://github.com/earthchie/jquery.Thailand.js/blob/master/jquery.Thailand.js/database/db.json))
- `vue-thailand-address.common.js`: สำหรับใช้กับ CommonJS/Node
- `vue-thailand-address.esm.js`: สำหรับใช้กับ ES module
- `db.js` (Unminified) และ `db.min.js` (Minified): เป็นไฟล์ฐานข้อมูลสำหรับใช้บร Browser
- `vue-thailand-address.js` (Unminified) และ `vue-thailand-address.min.js` (Minified): เป็นไฟล์ Vue plugin สำหรับใช้บน Browser

## 📚 API

ดูได้ที่ https://gluons.github.io/vue-thailand-address

## 📝 แผน

ดูได้ที่ https://github.com/gluons/vue-thailand-address/projects

## 👐 การช่วยเหลือ

- Fork repo นี้ สร้าง branch ใหม่ แล้วส่ง pull request 🙂
- ใช้ [Gitmoji](https://github.com/carloscuesta/gitmoji) กับข้อความ commit 😎

## 🤖 การพัฒนา

- ติดตั้ง dependencies

  ```bash
  npm install
  # หรือ
  yarn
  ```

- เปิดหน้าตัวอย่างที่ใช้พัฒนา  
  > (🙇 ขอขอบคุณ [⚡ Poi](https://github.com/egoist/poi) สำหรับ hot reload ที่ไม่ต้องเขียน config ให้ยุ่งยาก)

  ```bash
  npm run dev
  # หรือ
  yarn dev
  ```

- build ไฟล์

  ```bash
  npm run build
  # หรือ
  yarn build
  ```
