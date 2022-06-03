<!-- Please remove this file from your project -->
<template>
  <div id="main">
    <div id="nav">
      <img id="logo" src="favicon.ico"/>
      <div> Каталог </div>
      <div> О нас </div>
      <div> Контакты </div>
      <img id="cart" src="cart.png"/>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      player: "Игрок ХХХ"
    };
  },
  computed: {
    // a computed getter
    Win() {
      // `this` points to the vm instance
      if (this.healthMob < 1) {
        this.healthMob = 10;
        this.xp++;
        this.status.push(`Вы победили, ${this.player}`);
        this.status.push(`Вы получили 1 опыта, ${this.player}`);
        this.lowhp = true
        this.countTurn = 0
      }
    }
  },
  methods: {
    playerAttack() {
      this.turnMob = 1;
    }
  }
};
</script>

<style>
div { 
  width: 100%;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: center;
  vertical-align: middle;
}

#nav {
  /* nav/desktop */
  width: 100%;
  top: 0px;
  background: #d3eff0;
  display: inline-flex; 
}
#logo {
  /* logo */
  width: 100px;
  height: 50px;
}

#cart {
  /* Cart */
width: 26px;
height: 26px;
}
</style>