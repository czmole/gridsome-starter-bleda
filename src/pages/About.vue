<template>
  <Layout>
    <main>
      <header class="max-w-xl md:max-w-2xl xl:max-w-3xl mx-auto text-center px-6 pt-24">
        <h1 class="text-4xl sm:text-5xl md:text-6xl font-sans font-bold mb-1">Hello World!</h1>
      </header>
      <nav class="absolute top-0 left-0 z-20 mt-6 ml-6">
        <g-link to="/" class="text-gray-900 border-gray-400 text-sm border opacity-75 hover:opacity-100 rounded-full px-4 py-2 transition-opacity duration-300">&larr; Home</g-link>
      </nav>
      <article
        class="max-w-xl md:max-w-2xl xl:max-w-3xl mx-auto px-6 sm:px-12 pt-16 border-b border-gray-300 pb-10 mb-16">
        <div class="markdown text-lg leading-normal text-gray-700">
          <p>I am Catalin - web developer, father of two terrific twin boys, husband, and constant learner!</p>
          <p>I live in&nbsp;<a href="https://www.facebook.com/visitoradea/">Oradea, Romania</a>&nbsp;I am a self-taught
            web developer (Laravel, VueJs, NodeJs, LAMP/LEMP stack, web apps architecture, API
            design/development/integrations, payment processors integrations, etc) and passionate about all things
            related to the topic but also on the startups' world.</p>
          <h3 id="job">Job</h3>
          <p>I work at a local web studio&nbsp;<a href="http://www.11digits.com/">11Digits</a>&nbsp;were&nbsp;<a
              href="http://www.11digits.com/our-work/">we create great experiences</a>&nbsp;for small to medium
            businesses and startups from marketing websites (mainly WordPress projects) to medium/large web applications
            / CRM / ERP. So if you are in need of something like this, don&rsquo;t hesitate to&nbsp;<a
              href="http://www.11digits.com/contact/">give us a shout</a>.</p>
          <p>We are actively supporting and constantly improving&nbsp;<a href="https://www.taptasty.com/tour.php"
              target="_blank" rel="noopener">TapTasty.com</a> - we offer a full package of custom Android and iOS +
            infrastructure to manage your online selling and marketing campaigns if you have a business doing delivery,
            a restaurant, pizza&nbsp;place or something similar. We kicked off the first apps in production in the
            summer of 2019 and we have other customers that signed with us and that will be launching their apps in the
            first 3 months of 2020.</p>
          <p>Another project is&nbsp;<a
              href="https://www.inpreto.com/en/tour/clients-management/">Inpreto.com</a>&nbsp;a great tool to manage
            your customers, invoices, quotes, estimates, and expenses/income.</p>
          <h3 id="side-projects">Side Projects</h3>
          <p>One of my side projects is&nbsp;<a href="https://confdesk.com/">confdesk.com</a>&nbsp;- a SaaS that aims to
            help people running a call for papers, call for speakers for conferences, symposiums, sending invites,
            running peer reviews with their editor/reviewers, payments, reports, badges, etc - the current aim is to
            have a beta version by March 2018. The app is running a first version which is very old (10 years old code
            base and design) but the new version is meant to run as a subscription-based service/software.</p>
          <h3 id="volunteering">Volunteering</h3>
          <p>Starting 2017 I started to volunteer as time allows me with the great team from&nbsp;<a
              href="https://code4.ro/en/who-we-are/">Code4Romania</a>&nbsp; helping in various projects they have. Check
            on their projects to see how they help Romania develop and please consider a donation if you want to help
            these moving on <a href="https://code4.ro/en/donate/" target="_blank"
              rel="noopener">https://code4.ro/en/donate/</a></p>
          <p>🚀🔥❤⚡ They are really doing a great great job!</p>
          <h3 id="freelancing">Freelancing</h3>
          <p>As time permits I also do freelancing on small/medium size projects - preferably backend/server-side tasks.
          </p>
          <h3 id="this-blog">This blog</h3>
          <p>During the past 10-12 years, I have started several blogs, at the very early stage of blogging in Romania,
            dropped in several times because writing is not really me. But, the aim of my posts here is to share my
            findings, from my work, sharing solutions that I have found for problems that I got into. Many might be
            outdated but new to me but that way practicing writing helps improving it and helps me find the solution to
            a problem easier next time.</p>
          <h3 id="get-in-touch">Get in touch</h3>
          <p>You can find more about my findings, stuff that gets me busy and you can also send me direct messages via
            twitter&nbsp;<a href="https://twitter.com/czmole">@czmole</a></p>
          <p>Two quotes that I find inspiring for all the stuff you are doing/working on in this life, about doing the
            stuff you do with passion and fighting difficulties - both from <a
              href="https://en.wikipedia.org/wiki/Maya_Angelou" target="_blank" rel="noopener">Maya Angelou</a></p>
          <blockquote>
            <p><em>Success is liking yourself, liking what you do, and liking how you do it.&nbsp;</em></p>
          </blockquote>
          <blockquote>
            <p><em>If you don't like something, change it. If you can't change it, change your attitude.&nbsp;</em></p>
          </blockquote>
        </div>
      </article>
      <site-footer class="pb-8 sm:pb-10" />
    </main>
  </Layout>
</template>
<script>
import config from '~/.temp/config.js'
import SiteFooter from '@/components/Footer'

export default {
  components: {
    SiteFooter
  },
  metaInfo () {
    return {
      title: 'About',
      meta: [
        {
          key: 'description',
          name: 'description',
          content: this.ogDescription
        },

        { property: "og:type", content: 'article' },
        { property: "og:title", content:'About' },
        { property: "og:description", content: this.ogDescription },
        { property: "og:url", content: `${this.config.siteUrl}/about/` },
        { property: "og:image", content: this.ogImageUrl },

        { name: "twitter:card", content: "summary_large_image" },
        { name: "twitter:title", content: 'About' },
        { name: "twitter:description", content: this.ogDescription },
        { name: "twitter:site", content: "@cossssmin" },
        { name: "twitter:creator", content: "@cossssmin" },
        { name: "twitter:image", content: this.ogImageUrl },
      ],
    }
  },
  computed: {
    config () {
      return config
    },
    ogDescription () {
      return 'Introduction to the Bleda blog starter for Gridsome.'
    },
    ogImageUrl () {
      return `${this.config.siteUrl}/images/bleda-card.png`
    }
  },
}
</script>
