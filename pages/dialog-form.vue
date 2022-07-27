<template>

  <Dialog
      :visible="showProp"

      @update:visible="$emit('hideMethod')"
      @hideMethod="hideMethod"

      :style="{width: '450px'}"
      header="Product Details" :modal="true"
      class="p-fluid"
  >

    <div class="field">
      <InputText id="name" placeholder="Nome" required="true" autofocus/>
    </div>

    <div class="field">
      <InputText id="email" placeholder="E-mail" required="true" autofocus/>
    </div>

    <div class="field">
      <InputText id="Password" placeholder="Password" type="password" required="true" autofocus/>
    </div>

    <template #footer>
      <div class="my-2">
        <Button type="button" icon="pi pi-check" class="p-button-text" @click="$emit('saveMethod')"/>
        <Button type="button" icon="pi pi-times" class="p-button-text" @click="$emit('hideMethod')"/>
      </div>

    </template>

  </Dialog>

</template>

<script>
export default {
  name: "dialog-form",
  props: {
    showProp: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      hideMethod: false,

    }
  },

  methods: {},
}
</script>

<style scoped lang="scss">
@import '../../assets/demo/badges';
</style>