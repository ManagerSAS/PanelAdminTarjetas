<template>
  <div>
    <v-list>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title>Categoria 1</v-list-item-title>
        </v-list-item-content>
        <v-list-item-action>
          <v-btn icon @click="showItems = !showItems">
            <v-icon>{{ showItems ? 'mdi-chevron-up' : 'mdi-plus' }}</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
      <v-expand-transition>
        <v-list v-if="showItems">
          <v-list-item v-for="item in items" :key="item">
            <v-list-item-content>
              <v-list-item-title>{{ item }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-expand-transition>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title>Categoria 2</v-list-item-title>
        </v-list-item-content>
        <v-list-item-action>
          <v-btn icon @click="showItems2 = !showItems2">
            <v-icon>{{ showItems2 ? 'mdi-chevron-up' : 'mdi-plus' }}</v-icon>
          </v-btn>
        </v-list-item-action>
      </v-list-item>
      <v-expand-transition>
        <v-list v-if="showItems2">
          <v-list-item v-for="item in items2" :key="item">
            <v-list-item-content>
              <v-list-item-title>{{ item }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-expand-transition>
    </v-list>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showItems: false,
      showItems2: false,
      items: ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5'],
      items2: ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5']
    }
  }
}
</script>
