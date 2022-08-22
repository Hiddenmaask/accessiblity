<template>

  <div class="card-list" v-if="info">
    <article v-for="card in info" :key="card.id" class="card">
        <header class="card-header">
          <p>{{card.date}}</p>
          <h2>
          {{card.header}}
          </h2>
        </header>
        <div class="card-body">
          {{card.body}}

        </div>
        <div class="tags">
          <a href="#">{{card.tag[0]}}</a>
          <a href="#">{{card.tag[1]}}</a>
          <a href="#">{{card.tag[2]}}</a>
        </div>
    </article>
  </div>

</template>

<script>
export default {
  name: "CardList",
  data(){
    return{
      info: {
        card1: {id:1, "date": "09/08/22" , "header": "Putting Customers First", "body": "We put our customers first by putting them at the heart of everything we do. ", tag: ["css", "html", "web"] },
        card2: {id:2, "date": "09/08/22" , "header": "Damn yer mast, feed the sail.", "body": "Afterlife doesn’t harmoniously receive any monkey — but the thing is what converts.", tag: ["css", "html", "web"]  },
        card3: {id:3, "date": "09/08/22" , "header": "Treasure, faith, and life.", "body": "Karmas, cows, and celestine selfs will always protect them.", tag: ["css", "html", "web"]  },
        card4: {id:4, "date": "09/08/22" , "header": "How scrawny. You loot like a bucaneer.", "body": "Order is not the inward dogma of the monkey.", tag: ["css", "html", "web"]  },
        card5: {id:5, "date": "09/08/22" , "header": "Seashell of a heavy-hearted yellow fever, loot the endurance!", "body": "Neuter, placidus eras aliquando anhelare de castus, superbus tata.", tag: ["css", "html", "web"]  },
        card6: {id:6, "date": "09/08/22" , "header": "Collision course, life, and stigma.", "body": "Crush me captain, ye coal-black bung hole!", tag: ["css", "html", "web"]  },
        card7: {id:1, "date": "09/08/22" , "header": "Ah, evil hunger!", "body": "Well, sunny lubber. go to singapore. Galluss sunt lubas de audax secula. ", tag: ["css", "html", "web"] },
        card8: {id:2, "date": "09/08/22" , "header": "Damn yer mast, feed the sail.", "body": "Afterlife doesn’t harmoniously receive any monkey — but the thing is what converts.", tag: ["css", "html", "web"]  },
        card9: {id:3, "date": "09/08/22" , "header": "Treasure, faith, and life.", "body": "Karmas, cows, and celestine selfs will always protect them.", tag: ["css", "html", "web"]  },
        card10: {id:4, "date": "09/08/22" , "header": "How scrawny. You loot like a bucaneer.", "body": "Order is not the inward dogma of the monkey.", tag: ["css", "html", "web"]  },
        card11: {id:5, "date": "09/08/22" , "header": "Seashell of a heavy-hearted yellow fever, loot the endurance!", "body": "Neuter, placidus eras aliquando anhelare de castus, superbus tata.", tag: ["css", "html", "web"]  },
        card12: {id:6, "date": "09/08/22" , "header": "Collision course, life, and stigma.", "body": "Crush me captain, ye coal-black bung hole!", tag: ["css", "html", "web"]  },
      }
    }
  }
}
</script>

<style scoped>



.card-list {
  display: flex;
  padding: 5rem;
  overflow-x: scroll;
  scroll-behavior: smooth;
}

.card-list *{
  font-family: 'DM Mono', monospace;
}




.card-list::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}
.card-list::-webkit-scrollbar-thumb {
  background: hsl(var(--bg));
  border-radius: 10px;
  box-shadow: inset 2px 2px 2px hsla(0,0%,100%,.25), inset -2px -2px 2px rgba(0,0,0,.25);
}

.card-list::-webkit-scrollbar-track {
  background: linear-gradient(90deg,hsl(var(--bg)),hsl(var(--bg)) 1px,hsl(var(--accent)) 0,hsl(var(--accent)));
}


.card {
  display: flex;
  position: relative;
  flex-direction: column;
  text-align: center;
  height: 350px;
  width: 400px;
  min-width: 350px;
  padding: 1.5rem;
  border-radius: 16px;
  background: hsl(var(--bg));
  box-shadow: -1rem 0 3rem #000;

  transition: .2s;
}

.card:hover {
  transform: translateY(-1rem);
}

.card:hover~.card {
  transform: translateX(130px);
}


.card:not(:first-child) {
  margin-left: -130px;
}

.card-body{
  position: relative;
  display: grid;
  grid-template-columns: 1fr;
  align-items: center;
  margin: 3rem 0 0;
}

.tags {
  margin: 1rem 0 2rem;
  padding: .5rem 0 1rem;
  line-height: 2;
  margin-bottom: 0;
  float: bottom;
}

.tags a {
  font-style: normal;
  font-weight: 700;
  font-size: calc(var(--_size)/2);
  color: hsl(var(--accent));
  text-transform: uppercase;
  border: 3px solid hsl(var(--accent)/ .8);
  border-radius: calc(var(--_radius)*10);
  padding: .2rem .85rem .25rem;
  position: relative;
  transition: box-shadow var(--_tspeed_slow) var(--_ttype_squish),
  background-color var(--_tspeed_slow) var(--_ttype_squish);
}

.tags a:hover {

}

.tags a:where(:active, :hover) {
  background-color: hsl(var(--accent) / 0.7);
  box-shadow: 0 0 0 hsl(var(--accent) / 0.3), 0 0 0 -0.1em hsl(var(--bg)),
  0 0 0 -0.2em hsl(var(--accent));
  color: hsl(var(--bg));
}

.tags a:focus {
  outline: none;
}

.tags a:focus-visible {
  box-shadow: 0 0 0 hsl(var(--accent) / 0.3), 0 0 0 0.2em hsl(var(--bg)),
  0 0 0 0.4em hsl(var(--accent) / 0.7);
}

.card-body {
  margin-bottom: auto;
}

.card-header p {
  font-size: 14px;
  margin: 0 0 1rem;
  color: #7a7a8c;
}

.card-header h2 {
  font-size: 20px;
  margin: .25rem 0 auto;
  cursor: pointer;
}

.card-header h2:hover {
  background: linear-gradient(90deg,#ff8a00,#e52e71);
  text-shadow: none;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
</style>
