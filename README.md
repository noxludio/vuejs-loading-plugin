# vuejs-loading-plugin
Simple loading screen plugin for your Vue application

![Demonstration](https://raw.githubusercontent.com/noxludio/vuejs-loading-plugin/master/example.gif)

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
  background: 'rgb(255,255,255)', // set custom background
  classes: ['myclass'] // array, object or string
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
