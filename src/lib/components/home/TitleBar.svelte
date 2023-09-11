<div class="title-bar">
  <div class="window-button" />
  <div class="window-button" />
  <div class="window-button" />
</div>

<style lang="scss">
  div.title-bar {
    display: flex;
    justify-content: flex-end;
    align-items: center;

    min-height: 40px;
    padding: 0 5px;
    border-radius: 5px 5px 0 0;

    background-color: scale-color($color: $background, $lightness: -20%);

    div.window-button {
      height: 50%;
      aspect-ratio: 1;
      border-radius: 50%;
      margin: 0 5px;
      background-color: scale-color($color: $background, $lightness: 20%);
    }
  }
</style>
