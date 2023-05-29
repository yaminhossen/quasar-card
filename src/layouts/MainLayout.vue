<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>
        <div>
          <RouterLink  id="links" to="/carts">Cart</RouterLink> <br>
          <RouterLink id="links" to="/products">All Product</RouterLink>
        </div>
        <!-- <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        /> -->
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import Cart from 'src/components/Carts.vue'
import Products from 'src/components/Products.vue'



export default defineComponent({
  name: 'MainLayout',

  components: {
     Cart, Products
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
<style scoped>
#links{
  text-decoration: none;
  font-size: 25px;
  font-weight: 700;
  cursor: pointer;
  background-color: rgb(165, 164, 164);
  display: block;
  color: rgb(104, 103, 103);
  padding-left: 20px;
}
#links:hover{
  background-color: rgb(81, 79, 79);
  color: white;
}
</style>
