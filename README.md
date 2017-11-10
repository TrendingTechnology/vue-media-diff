# vue-media-diff [![Build Status](https://travis-ci.org/MKFMIKU/vue-media-diff.svg?branch=master)](https://travis-ci.org/MKFMIKU/vue-media-diff)

> A component to diff image or video with Vue.js Edit
  Add topics
  
[![forthebadge](http://forthebadge.com/images/badges/uses-js.svg)](http://forthebadge.com)
[![forthebadge](http://forthebadge.com/images/badges/built-with-love.svg)](http://forthebadge.com)
  
## Installation

```bash
npm install vue-media-diff -s
```

## Usage
```js
import MediaDiff from './Component.vue';

  export default {
    name: 'app',
    data() {
      return {
        origin: "src/assets/origin.jpg",
        diff: "src/assets/diff.jpg"
      }
    },
    components: {
      MediaDiff
    },
  }
```

```html
<MediaDiff :origin="origin"
           :diff="diff"
           style="width: 540px; height: 400px">
</MediaDiff>
```
![](https://ooo.0o0.ooo/2017/11/10/5a0565569b03f.png)


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
