<template>
  <main id="news" class="page-container">
    <header class="app-bar-top">
      <h1>
        <a href="#" class="logo">
          <i class="material-icons">menu</i>
        </a>
        Hacker News
      </h1>
      <div class="app-bar-top__right">
        <a href="#"><i class="material-icons">account_circle</i></a>
      </div>
    </header>
    <nav>
      <ul class="tabs">
        <li class="tabs__tab tabs__tab--active"><a href="#">New</a></li>
        <li class="tabs__tab"><a href="#">Comments</a></li>
        <li class="tabs__tab"><a href="#">Show</a></li>
        <li class="tabs__tab"><a href="#">Ask</a></li>
        <li class="tabs__tab"><a href="#">Jobs</a></li>
      </ul>
    </nav>

    <section class="articles">
      <article class="card" v-for="article in articles" v-bind:key="article.id">
        <header class="card__header">
          <h3 class="card__secondary-text">
            {{ article.source }}
          </h3>

          <h2 class="card__primary-title">
            <a v-bind:href="article.url">
              {{ article.title}}
            </a>
          </h2>

          <p class="card__supporting-text">
            {{ article.points }}pt
            by
            <a v-bind:href="'https://news.ycombinator.com/user?id=' + article.user">
              {{ article.user }}
            </a>
            {{article.when}}min ago
          </p>
        </header>

        <section class="card__actions">
          <div class="card__actions--left">
            <a v-bind:href="'https://news.ycombinator.com/item?id=' + article.link"
               class="button--text">
              Discuss
            </a>
          </div>
          <div class="card__actions--right">
            <a v-bind:href="'https://hn.algolia.com/?query=' + article.title"
               class="button--icon">
              <i class="material-icons">history</i>
            </a>
            <a v-bind:href="'https://news.ycombinator.com/hide?id=' + article.link + '&goto=news'"
               class="button--icon">
              <i class="material-icons">visibility_off</i>
            </a>
          </div>
        </section>
      </article>
    </section>

    <a href="javascript:void(0)" class="fab">
      <i class="material-icons">add</i>
    </a>

  </main>
</template>

<script>
var articles = [
  {
    title: 'MIT 9.11: The Human Brain (Spring 2018)',
    source: 'mit.edu',
    url: 'https://nancysbraintalks.mit.edu/course/9-11-the-human-brain',
    link: '17216634',
    user: 'indescions_2018',
    points: 33,
    when: '6/2/2018 3:22pm'

  },
  {
    title: 'OpenDUNE – An open-source recreation of the game Dune II ',
    source: 'github.com',
    url: 'https://github.com/OpenDUNE/OpenDUNE',
    link: '17214320',
    user: 'marluz',
    points: 351,
    when: '6/2/2018 1:15pm'
  },
  {
    title: 'Deep learning: a critical appraisal',
    source: 'arxiv.org',
    url: 'https://arxiv.org/abs/1801.00631',
    link: '17216536',
    user: 'fanf2',
    points: 17,
    when: ''
  },
  {
    title: 'Wage Theft is a Bigger Problem Than Other Forms of Theft',
    source: 'epi.org',
    url: 'https://www.epi.org/publication/wage-theft-bigger-problem-forms-theft-workers/',
    link: '17216319',
    user: 'waiterbell',
    points: 104
  },
  {
    title: 'Linux Cryptography: Speck\'s real standing with the academic community',
    url: 'https://www.spinics.net/lists/linux-crypto/msg33291.html',
    source: 'spinics.net',
    link: '17214827',
    user: 'zx2c4',
    points: 170
  },
  {
    title: 'Apple Looks to Expand Advertising Business with New Network for Apps',
    url: 'https://www.wsj.com/articles/apple-looks-to-expand-advertising-business-with-new-network-for-apps-1527869990',
    source: 'wsj.com',
    link: '17215391',
    user: 'maltalex',
    points: 68
  },
  {
    title: 'One year of C ',
    url: 'http://floooh.github.io/2018/06/02/one-year-of-c.html',
    source: 'github.io',
    link: '17216039',
    user: 'gok',
    points: 142
  }
]

export default {
  name: 'News',
  data () {
    return {
      articles: articles
    }
  }
}
</script>

<style scoped>
.articles {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin: 8px;
}
</style>
