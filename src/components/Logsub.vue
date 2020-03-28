<template>
<div class="Logsub">
  <div class="wrapper">
    <div class="Logsub__flex">
      <div class="Logsub__log">
        <div class="Logsub__title">Member login</div>
        <div class="Logsub__inputs">
          <div class="Logsub__name">
            <input class="Logsub__input" minlength="1" required maxlength="8" type="pass" placeholder="User name">
          </div>
          <div class="Logsub__pass">
            <input class="Logsub__input" minlength="5" required maxlength="15" type="password" placeholder="Password">
          </div>
          <button class="Logsub__btn">Log me in</button>
        </div>
      </div>
      <div class="Logsub__sub">
        <div class="Logsub__title">Subscribe to our weekly newsletter</div>
        <div class="Logsub__inputs">
          <div class="Logsub__email">
            <input class="Logsub__input" minlength="5" required maxlength="15" type="email" placeholder="email address">
          </div>
          <button class="Logsub__btn">Subscribe</button>

        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Logsub'
}
</script>

<style lang="scss">
.Logsub {
  position: relative;
  padding: rem(20) 0;
  &__flex {
    @include FCenter(space-between);
  }
  &__title {
    color: white;
    font-size: rem(26);
    font-weight: normal;
  }
  &__log, &__sub {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: rem(80);
    width: rem(430);
    padding: rem(15) rem(15) rem(15) rem(25);
    background-color: $orange;
  }
  &__sub {
    background-color: $lightblue;
  }
  &__inputs {
    @include FCenter(space-between);
    height: rem(30);
  }
  &__input {
    box-sizing:border-box;
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    transition-duration: .5s;
    padding-left: rem(10);
  }
  &__input:focus {
    background-color: lightblue;
  }
  &__name, &__pass, &__email {
    height: 100%;
    width: rem(140);
  }
  &__email {
    width: rem(265);
  }
  &__btn {
    padding: rem(5) rem(15);
    border: 1px solid $blackbtn;
    outline: none;
    background-color: $blackbtn;
    color: white;
    transition-duration: .5s;
    font-size: rem(16);
  }
  &__btn:hover {
    background-color: white;
    color: $blackbtn;
    cursor: pointer;
  }

}
.Logsub:before {
  content: "";
  position: absolute;
  height: 1px;
  width: 100%;
  background-color: $before;
  top: rem(-15);
}
</style>
