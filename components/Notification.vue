<template>
  <div></div>
</template>

<script>
export default {
  name: 'notification',
  props: [
    'icon',
    'color',
    'position',
    'sticky',
    'duration',
    'progress',
    'title',
    'text',
  ],
  computed: {
    getIcon() {
      return `<span class='material-icons'>${
        this.icon ? this.icon : 'check_circle'
      }</span>`
    },
  },
  mounted() {
    this.$vs.notification({
      icon: this.getIcon,
      color: this.color || null,
      duration: this.duration || null,
      progress: this.progress || 'auto',
      position: this.position || null,
      title: this.title,
      text: this.text,
      sticky: this.sticky || false,
    })
  },
}
</script>
