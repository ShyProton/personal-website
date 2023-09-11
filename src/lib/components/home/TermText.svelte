<div class="text">
  <div class="term-text">
    <h2>
      <span class="prompt">[system:~]$</span>
      <span class="command">whoami</span>
    </h2>
    <h2 class="name">Shayan Rashid</h2>
  </div>
  <div class="extra-text">
    <h3>I'm a developer!</h3>
    <h3>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda magnam
      nostrum quae voluptas eos! Laboriosam iusto eaque obcaecati facilis
      inventore possimus adipisci odio. Voluptatibus accusamus illo ipsa maxime
      cumque! Architecto?
    </h3>
  </div>
</div>

<style lang="scss">
  div.text {
    div.term-text {
      margin-bottom: 20px;

      h2 {
        font-family: "Fira Code", monospace;
        color: $foreground;

        &.name {
          animation: flicker 1.5s ease-in-out infinite alternate;
        }

        span.prompt {
          color: $light-green;
        }

        span.command {
          color: $light-yellow;
        }
      }
    }

    div.extra-text {
      h3 {
        color: $foreground;
      }
    }
  }

  @include md {
    div.text {
      div.extra-text {
        width: 50%;
      }
    }
  }

  @keyframes flicker {
    0%,
    18%,
    22%,
    25%,
    53%,
    57%,
    100% {
      text-shadow: 0 0 4px $light-yellow, 0 0 11px $light-yellow,
        0 0 19px $light-yellow, 0 0 40px $dark-yellow, 0 0 80px $dark-yellow,
        0 0 90px $dark-yellow, 0 0 100px $dark-yellow, 0 0 150px $dark-yellow;
    }

    20%,
    24%,
    55% {
      text-shadow: none;
    }
  }
</style>
