#### Vuex Web3 Plugin

This plugin makes it simple to add web3 wallet support to any Vue website powered by Ethers.js 
 
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
    web3Storage
  }


})

```



## How to use in Frontend 

#### Connect to wallet 


          await this.$store.commit('setInjectedEthereum',window.ethereum)
          
          await this.$store.dispatch('connect')



#### Disconnect from wallet 

          await this.$store.dispatch('disconnect')



#### Get connected account publiic address
        

         let publicAddress = this.$store.state.web3Storage.account


### get injected provider 

        let injectedEthereum = this.$store.state.web3Storage.injectedEthereum

        let provider = new ethers.providers.Web3Provider(injectedEthereum)
