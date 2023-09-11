<script lang="ts">
  import { page } from "$app/stores";

  export let name: string;
  const href = `#${name.toLowerCase()}`;

  $: active = $page.url.hash == href;

  let scrollToSection = (id: string) => {
    const element = document.getElementById(id);
    element?.scrollIntoView({ behavior: "smooth" });
  };
</script>

<li>
  <a
    {href}
    class:active
    on:click|preventDefault={() => scrollToSection(name.toLowerCase())}
    >{name}</a
  >
</li>

<style lang="scss">
  li {
    a {
      display: flex;
      justify-content: center;
      align-items: center;

      transition: background-color 0.1s linear;
      text-decoration: none;
      color: $foreground;

      width: 100%;

      &:hover {
        background-color: scale-color($color: $background, $lightness: 10%);
      }

      &.active {
        background-color: scale-color($color: $background, $lightness: 20%);
      }
    }
  }

  @include sm {
    li {
      height: 100%;
      width: 100%;
      max-width: 250px;

      a {
        height: 100%;
      }
    }
  }
</style>
