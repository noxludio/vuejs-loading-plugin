# vuejs-loading-plugin
Simple loading screen plugin for your Vue application

## Getting Started
Install
```
npm i --save vuejs-loading-plugin
```

Set up
```javascript
import VueLoading from 'vuejs-loading-plugin'

// using default options
Vue.use(VueLoading)

// overwrite defaults
Vue.use(VueLoading, {
  dark: true, // default false
  text: 'Ladataan', // default 'Loading'
  loading: true, // default false
  customLoader: myVueComponent, // replaces the spinner and text with your own
  background: 'rgb(255,255,255)', // provice custom background
  classes: ['myclass'] // Array, object or string
})
```

Usage
```javascript
// set loading state manually in components
this.$loading(true)
this.$loading(false)

// use async function
// takes promise and returns a promise
import { asyncLoading } from 'vuejs-loading-plugin'

const login = new Promise( (resolve, reject) => {
  // api call
})
asyncLoading(login).then().catch()
```
