<template>
  <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
  >
    <v-list>
      <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title"/>
        </v-list-item-content>
      </v-list-item>
      <v-list-item>
        <v-list-item-action @click.stop="miniVariant = !miniVariant" >
          <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
        </v-list-item-action>
      </v-list-item>
    </v-list>

  </v-navigation-drawer>
</template>
<script>
export default {
  name: 'navigation-drawer',
  props: {
    clipped: {},
    drawer: {},
    items: {},
    miniVariant: {}
  }
}
</script>
