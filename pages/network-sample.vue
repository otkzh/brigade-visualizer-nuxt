<template>
  <v-container>
    <network
      id="mynetwork"
      ref="network"
      style="height: 500px"
      :nodes="nodes"
      :edges="edges"
      :options="options"
    >
    </network>
  </v-container>
</template>
<script>
import { Network } from 'vue-visjs'
export default {
  components: {
    network: Network,
  },
  data() {
    return {
      nodes: [
        { id: 1, label: 'Node 1' },
        { id: 2, label: 'Node 2' },
        { id: 3, label: 'Node 3' },
        { id: 4, label: 'Node 4' },
        { id: 5, label: 'Node 5' },
      ],
      edges: [
        { from: 1, to: 3 },
        { from: 1, to: 2 },
        { from: 2, to: 4 },
        { from: 2, to: 5 },
        { from: 3, to: 3 },
      ],
      options: {},
    }
  },
}
</script>

