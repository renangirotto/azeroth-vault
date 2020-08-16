<template>
  <div class="c-reputation">
    <h3 class="c-reputation__title">Battle for Azeroth</h3>
    <ul class="c-reputation__list">
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--hated" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--hostile" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--unfriendly" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--neutral" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--friendly" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--honored" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--revered" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--exalted" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
      <li class="c-reputation__list__item">
        <a href="#" target="_blank">Faction Name</a>
        <div class="c-reputation__list__item__progress--paragon" data-info="Neutral - 500/1000">
          <span style="width:50%" data-max="100" data-value="80"></span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "c-reputation",
};
</script>

<style lang="scss" scoped>
.c-reputation {
  // title for expansion names (h3)
  @include element(title) {
    font-weight: 700;
    font-size: 28px;

    &:not(:last-child) {
      margin-bottom: 16px;
    }
  }

  // list of faction name + reputation progress
  @include element(list) {
    // individual faction
    @include element(item) {
      &:not(:last-child) {
        margin-bottom: 12px;
      }

      // container of name + progress
      a {
        color: $c-light-100;
        text-decoration: none;

        &:hover {
          text-decoration: underline;
        }
      }

      // progress bar + info text inside it
      @include element(progress) {
        box-sizing: border-box;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 32px;
        border: 2px solid $c-dark-900;
        border-radius: 4px;
        position: relative;
        margin-top: 4px;
        background-color: $c-dark-600;
        overflow: hidden;

        // Info text
        &::after {
          content: attr(data-info);
          position: relative;
          z-index: $z-lvl-1;
        }

        // progress bar
        span {
          display: block;
          height: 100%;
          border: none;
          position: absolute;
          top: 0;
          left: 0;
          z-index: $z-lvl-1;
        }

        // progress color modifier
        @include modifier(hated) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-red;
          }
        }

        @include modifier(hostile) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-red;
          }
        }

        @include modifier(unfriendly) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-red;
          }
        }

        @include modifier(neutral) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-yellow;
          }
        }

        @include modifier(friendly) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-green;
          }
        }

        @include modifier(honored) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-green;
          }
        }

        @include modifier(revered) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-green;
          }
        }

        @include modifier(exalted) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-green;
          }
        }

        @include modifier(paragon) {
          @extend .c-reputation__list__item__progress;

          span {
            background-color: $c-reputation-blue;
          }
        }
      }
    }
  }
}
</style>