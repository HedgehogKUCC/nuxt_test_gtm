<template>
  <div>
    <Tutorial />
    <el-button @click="triggerGTM">
      GTM push event
    </el-button>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  methods: {
    triggerGTM () {
      window.dataLayer = window.dataLayer || []

      window.dataLayer.push({
        event: 'click_generateObituary',
        obituary_id: 9999,
        erp_case_id: '1234567890'
      })
    }
  }
}
</script>
