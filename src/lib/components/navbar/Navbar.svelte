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
      <li>
        <a href="#home">Home</a>
      </li>
      <li>
        <a href="#projects">Projects</a>
      </li>
      <li>
        <a href="#experience">Experience</a>
      </li>
    </ul>
  </div>
</nav>
<div class="spacer" />

<style lang="scss">
  $nav-height-sm: 80px;
  $nav-height-md: 50px;

  nav {
    position: fixed;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    top: 0;
    width: 100%;
    height: $nav-height-sm;
    padding: 0 0px;

    @include sm {
      height: $nav-height-md;
    }

    color: $foreground;
    background-color: scale-color($color: $background, $lightness: -30%);

    div.title {
      width: 80%;

      @include sm {
        width: 50%;
      }

      h1 {
        display: flex;
        flex-direction: row;

        font-size: 7vw;
        padding-left: 20px;

        @include sm {
          font-size: 1.5em;
        }
      }
    }

    div.links {
      display: flex;
      justify-content: flex-end;
      align-items: center;

      height: 100%;

      @include sm {
        width: 50%;
      }

      .nf {
        cursor: pointer;

        margin-right: 20px;
        font-size: 7vw;

        @include sm {
          display: none;
        }
      }

      ul {
        display: none;
        list-style-type: none;

        li {
          display: flex;
          justify-content: center;
          align-items: center;
        }
      }

      @include sm {
        ul {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          width: 100%;
          height: 100%;

          li {
            height: 100%;
            width: 100%;
            max-width: 250px;
            background-color: scale-color($color: $background, $lightness: 30%);
          }
        }
      }
    }
  }

  .spacer {
    margin-bottom: $nav-height-sm;

    @include sm {
      margin-bottom: $nav-height-md;
    }
  }
</style>
