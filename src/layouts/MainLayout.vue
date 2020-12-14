<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title class="absolute-center">
          {{ title }}
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL} from'quasar'
export default {
  computed:{
    title() {
     console.log(this.$route)
     let currentPath =this.$route.fullPath
     if(currentPath == '/')
     {
       return 'chatapp'
     }
     else if(currentPath == '/auth')
      {
        return 'login'
        }
     else if(currentPath == '/user') 
     {return 'user'
     }
     return 0
 }
  },
  methods: {
    openURL
  }
}
</script>
<style>
</style>