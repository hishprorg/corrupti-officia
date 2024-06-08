# @hishprorg/corrupti-officia

> `@hishprorg/corrupti-officia` is a tiny React Hook, designed  to easily add a loader to all your axios instances.

[![NPM](https://img.shields.io/npm/v/@hishprorg/corrupti-officia.svg)](https://www.npmjs.com/package/@hishprorg/corrupti-officia) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## ⚙️ Installation

```bash
npm install --save @hishprorg/corrupti-officia
```
or
```bash
yarn add @hishprorg/corrupti-officia
```

## 🚀 Usage

```jsx
import React, { Component } from 'react'
import axiosInstance from 'axios'

import { useAxiosLoader } from '@hishprorg/corrupti-officia'

const MyComponent = () => {
  // Pass the axios instance to the hook
  // Allows you tu customize easily your instance
  const [loading] = useAxiosLoader(axiosInstance)
  return (
    <>
      {loading
      ? <img src="path/to/loader"}/>
      : <div>My data</div>
      }
    </>
  )
}
```

You may also pass an array of URLs to ignore. This is the second parameter accepted by this hook.

```jsx
const ignoredUrls = ['https://myignoredurl.com', 'anotherignored.co']
const [loading] = useAxiosLoader(axiosInstance, ignoredUrls)
```

All urls passed in the `ignoredUrls` variable, won't trigger the loader.

## License

MIT © [olivier1208](https://github.com/olivier1208)

---
