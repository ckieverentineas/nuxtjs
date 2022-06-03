<!-- Please remove this file from your project -->
<template>
  <div id="main">
    <div id="nav">
      <img id="logo" src="favicon.ico"/>
      <a id="order"> Каталог</a>
      <a id="about"> О нас</a>
      <a id="contact"> Контакты</a>
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
  display: flex;
}
#main {
  text-align: center;
  justify-content: center;
  vertical-align: middle;
  margin-left: auto;
  margin-right: auto;
  display: flex;
}
#nav {
  /* nav/desktop */
  position: absolute;
  width: 1440px;
  height: 75px;
  left: 0px;
  top: 0px;
  background: #d3eff0;
  display: inline-flex; 
}
#logo {
  /* logo */
position: absolute;
width: 100px;
height: 50px;
left: 165px;
top: 20px;
}
#order {
  /* Discovery */
  position: absolute;
  width: 85px;
  height: 25px;
  left: 533px;
  top: 25px;
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #272727;
}
#about {
  /* About */
position: absolute;
width: 129px;
height: 25px;
left: 655px;
top: 25px;
font-family: 'Roboto';
font-style: normal;
font-weight: 500;
font-size: 16px;
line-height: 19px;
display: flex;
align-items: center;
text-align: center;
color: #272727;
}

#contact {
  /* Contact us */


position: absolute;
width: 130px;
height: 25px;
left: 790px;
top: 25px;

font-family: 'Roboto';
font-style: normal;
font-weight: 500;
font-size: 16px;
line-height: 19px;
display: flex;
align-items: center;
text-align: center;

/* black */

color: #272727;
}
#cart {
  /* Cart */


position: absolute;
width: 26px;
height: 26px;
left: 1244px;
top: 24px;
}
</style>