<script lang="ts">
  import TitleBar from "./TitleBar.svelte";
  import TermText from "./TermText.svelte";
</script>

<div class="container">
  <div class="terminal">
    <TitleBar />
    <div class="contents">
      <TermText />
      <div class="icons" />
    </div>
  </div>
</div>

<style lang="scss">
  div.container {
    display: flex;
    justify-content: center;
    align-items: center;

    height: 50vh;

    div.terminal {
      display: flex;
      flex-direction: column;

      width: 90%;
      height: 90%;

      animation: ease-in-out terminal-open 0.75s;

      border-radius: 5px;
      background-color: scale-color($color: $background, $lightness: 10%);
      border: 2px solid scale-color($color: $background, $lightness: 20%);

      div.contents {
        display: flex;

        height: 100%;
        padding: 10px;

        div.icons {
          aspect-ratio: 1;
          width: 0;
        }
      }
    }
  }

  @include sm {
    div.container {
      height: 60vh;
    }
  }

  @keyframes terminal-open {
    from {
      transform: scale(0);
      opacity: 0;
    }
    to {
      transform: scale(1);
      opacity: 1;
    }
  }
</style>
