#### Vuex Web3 Plugin

 
## How to Install


In a vue project, add to **main.js**:


```

import Vuex from 'vuex'

  
import web3Storage from "vuex-web3-plugin";

Vue.use(Vuex)
export const store = new Vuex.Store({
  state: {},
  getters: {},
  mutations: {},
  actions: {},
  modules: {
    web3Storage,
    shoppingCart,
    frontendStorage 
  }


})

```