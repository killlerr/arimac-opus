<template>
    <div>
        {{info}}
    </div>
</template>

<script>
export default {
    data () {
        return {
        info: null
        }
    },
    mounted () {
    this.$axios
      .get('http://opus-api.devops.arimac.xyz/webapi/projects/')
      .then(response => (this.info = response))
    }
}
</script>
