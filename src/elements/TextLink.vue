<template>
  <a :href="href" :target="target">
    <slot/>
  </a>
</template>

<script>
  export default {
    name: 'TextLink',
    props: {
      /**
       * The URL for the link
       */
      href: {
        default: '#',
        required: true
      },
      /**
       * Specifies where to display the linked URL.
       * `_self, _blank, _parent, _top`
       */
      target: {
        type: String,
        default: '_self'
      }
    }
  };
</script>

<style lang="scss" scoped>
  a {
    @include reset;
    font-family: $font-family-primary;
    color: $color-primary-vermilion;
    text-decoration: underline;
  }
</style>

<docs>
  ```jsx
  <text-link href="https://viljamisdesign.com">I am a link!</text-link>
  ```
</docs>
