<template>
  <div id="app">
    <Header />
    <main>
      <CardList :cards="themeCards" @card-clicked="handleCardClicked">
      </CardList>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import CardList from './components/CardList.vue';

export default {
  data() {
    return {
      themeCards: [
        { title: 'Suspiria', description: 'An American newcomer to a prestigious German ballet academy comes to realize that the school is a front for something sinister amid a series of grisly murders.' },
        { title: 'Scanners', description: 'A scientist trains a man with an advanced telepathic ability called "scanning" to stop a dangerous Scanner with extraordinary psychic powers from waging war against non scanners.' },
        { title: 'Martyrs', description: 'A young womans quest for revenge against the people who kidnapped and tormented her as a child leads her and a friend, who is also a victim of child abuse, on a terrifying journey into a living hell of depravity.' },
        { title: 'The Thing', description: 'A research team in Antarctica is hunted by a shape-shifting alien that assumes the appearance of its victims.' },
        { title: 'Repulsion', description: 'A sex-repulsed woman who disapproves of her sisters boyfriend sinks into depression and has horrific visions of rape and violence.' },
        { title: 'The Tenant', description: 'A bureaucrat rents a Paris apartment where he finds himself drawn into a rabbit hole of dangerous paranoia' },
      ],
    };
  },
  methods: {
    handleCardClicked(card) {
      console.log('Card clicked:', card.title);
    },
  },
  components: {
    Header,
    Footer,
    CardList,
  },
};
</script>

