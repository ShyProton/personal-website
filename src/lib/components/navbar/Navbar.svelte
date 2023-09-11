<script lang="ts">
  import NavLink from "./NavLink.svelte";
</script>

<nav>
  <div class="title">
    <h1>
      <div class="nf nf-dev-terminal" />
      &nbsp; Shayan | Portfolio
    </h1>
  </div>
  <div class="links">
    <div class="nf nf-md-menu" />
    <ul>
      <NavLink name="Home" />
      <NavLink name="Projects" />
      <NavLink name="Experience" />
    </ul>
  </div>
</nav>
<div class="spacer" />

<style lang="scss">
  $nav-height: 80px;

  nav {
    position: fixed;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    top: 0;
    width: 100%;
    height: $nav-height;
    padding: 0 0px;

    color: $foreground;
    background-color: scale-color($color: $background, $lightness: -30%);

    div.title {
      width: 80%;

      h1 {
        display: flex;
        flex-direction: row;

        font-size: clamp(1em, 7vw, 2em);
        padding-left: 20px;
      }
    }

    div.links {
      display: flex;
      justify-content: flex-end;
      align-items: center;

      height: 100%;

      .nf {
        cursor: pointer;

        margin-right: 20px;
        font-size: clamp(1em, 7vw, 2em);
      }

      ul {
        display: none;
        list-style-type: none;
      }
    }
  }

  .spacer {
    margin-bottom: $nav-height;
  }

  @include sm {
    $nav-height: 50px;

    nav {
      height: $nav-height;

      div.title {
        width: 50%;

        h1 {
          font-size: 1.5em;
        }
      }

      div.links {
        width: 50%;

        div.nf {
          display: none;
        }

        ul {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          width: 100%;
          height: 100%;
        }
      }
    }

    .spacer {
      margin-bottom: $nav-height;
    }
  }
</style>
