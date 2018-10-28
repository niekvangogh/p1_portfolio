<template>
  <b-row>
    <b-col lg="6">
      <h1>Portfolio website</h1>
      <p>
        Afgelopen weken (week 7 en 8) heb ik gewerkt aan een website om mijn portfolio op te zetten voor media. Ik heb
        erg hard mijn best gedaan om een creatief design te realiseren voor deze website, maar door mijn lack van
        creativiteit vond ik dit erg moeilijk. Ik heb geprobeerd mijn best te doen, en hoop dat jullie tevreden zijn met
        het resultaat.
      </p>
      <p>
        Op de pagina <a href="/betekenis">Wat betekend deze website voor MIJ?</a> heb ik beschreven wat het maken van
        deze website heeft
        betekend voor mij, op het vlak van ICT & media.
      </p>
    </b-col>
    <b-col lg="6">
      <h2>Niek, deze website zuigt ballen?! Waarom is dit goed genoeg voor media?</h2>
      <p>
        Ik ben blij dat je je dat ook afvraagd, ik ben er volledig mee eens dat deze website niet het beste design
        heeft, of de beste user experience, maar ik ben er van overtuigd dat hier toch een HEEL aantal wat media
        elementen in zijn verwerkt. De volgende lijst geeft een aantal punten aan waar ik echt op heb gelet om deze
        website zo goed mogelijk te maken.
      </p>
      <ul>
        <li>Deze website is VOLLEDIG responsive en mobiel vriendelijk.</li>
        <li>Deze website is SEO geoptimaliseerd (Search Engine Optimalisation)</li>
        <li>Deze website is gemaakt in een Nuxt.js (een framework) en is verschrikkelijk snel.</li>
        <li>Deze website is heeft een geavanceerd routing systeem (url)</li>
         </ul>
    </b-col>
    <b-col lg="6">
      <h2>Week 7</h2>
      <p>
        In week 7 heb ik een start gemaakt aan de website, niet veel. Ik heb die dag het meest klasgenoten geholpen met
        hun websites, zodat ze verder konden. Ik heb dit gedaan tot ongeveer 14.00 en ben zelf toen verder gegaan aan
        mijn website.
      </p>
      <p>
        Het design van de website heb ik erg abstract gehouden met een gebruik van Bootstrap om het makkelijk en
        overzichtelijk te houden.
      </p>
    </b-col>
    <b-col lg="6">
      <h2>Week 8</h2>
      <p>
        In week 8 heb ik tijdens de les niet heel veel aan mijn website gewerkt, een beetje het zelfde verhaal als bij
        week 7. Ik heb veel van mijn klasgenoten geholpen zodat ze verder kunnen, ik weet al hoe ik websites kan maken,
        mijn klasgenoten niet. Dus als ik ze help, kunnen ze vooruit. Ik vind het erg leuk om andere te helpen in
        programmeren, op een goede manier zodat ze het kunnen snappen.
      </p>
      <p>
        Ik heb de rest van de website gemaakt in het weekend van de oplevering.
      </p>
    </b-col>
    <b-col lg="6">
      <h2>
        Website iteraties
      </h2>
      <p>
        Ik heb de verschillende iteraties van mijn websites niet geupload, maar ik heb alles geupload naar GitHub en
        geprobeerd zo goed mogelijk bij te houden.
      </p>
      <ul>
        <li v-for="record in commits">
          <a :href="record.html_url" target="_blank" class="commit">{{ record.sha.slice(0, 7) }}</a>
          - <span class="message">{{ record.commit.message | truncate }}</span>
        </li>
      </ul>

      <p>
        Als je op de commit klikt, kun je zien wat er is veranderd per iteratie, per toevoeging van de website.
      </p>

    </b-col>
  </b-row>
</template>
<script>

  export default {
    data() {
      return {
        currentBranch: 'master',
        commits: null,
        apiURL: 'https://api.github.com/repos/nivyox/p1_portfolio/commits?per_page=100'
      }
    }, created: function () {
      this.fetchData()
    }, watch: {
      currentBranch: 'fetchData'
    }, filters: {
      truncate: function (v) {
        let newline = v.indexOf('\n');
        return newline > 0 ? v.slice(0, newline) : v
      }, formatDate: function (v) {
        return v.replace(/T|Z/g, ' ')
      }
    }, methods: {
      async fetchData() {
        let self = this;
        const result = await this.$axios.get(this.apiURL);
        self.commits = result.data;
      }
    }
  }
</script>
