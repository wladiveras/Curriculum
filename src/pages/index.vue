<script setup lang="ts">

const { t } = useI18n()

const data = {
  name: 'Wladi Veras',
  stack: '',
  contacts: {
    email: {
      icon: 'mdi-email',
      label: 'hi@wladi.com.br',
      value: 'mailto:hi@wladi.com.br',
    },
    phone: {
      icon: 'mdi-phone',
      label: '+55 (21) 96909-8986',
      value: 'tel:+5521969098986',
    },
    github: {
      icon: 'carbon-logo-github',
      label: '#wladiveras',
      value: 'https://github.com/wladiveras',
    },
    youtube: {
      icon: 'carbon-logo-youtube',
      label: '@WladiVeras',
      value: 'https://www.youtube.com/channel/UCGf8DWazIyaIQ32dKTCpRXg',
    },
  },
  skills: {
    Laravel: {
      icon: 'mdi-laravel',
      label: 'Laravel',
      main: true,
      learning: false,
    },
    php: {
      icon: 'cib:php',
      label: 'PHP',
      main: true,
      learning: false,
    },
    cakephp: {
      icon: 'cib:cakephp',
      label: 'CakePHP',
      main: false,
      learning: false,
    },
    apirest: {
      icon: 'dashicons:rest-api',
      label: 'API REST',
      main: true,
      learning: false,
    },
    ts: {
      icon: 'file-icons:typescript-alt',
      label: 'TypeScript',
      main: false,
      learning: true,
    },
    js: {
      icon: 'akar-icons:javascript-fill',
      label: 'JavaScript',
      main: false,
      learning: true,
    },
    html: {
      icon: 'ion:logo-html5',
      label: 'HTML5',
      main: false,
      learning: false,
    },
    css3: {
      icon: 'ion:logo-css3',
      label: 'Css3',
      main: false,
      learning: false,
    },
    linux: {
      icon: 'cib:linux',
      label: 'Linux',
      main: false,
      learning: false,
    },
    nodejs: {
      icon: 'bx:bxl-nodejs',
      label: 'NodeJS',
      main: false,
      learning: false,
    },
    sass: {
      icon: 'ion:logo-sass',
      label: 'SasS',
      main: false,
      learning: false,
    },
    git: {
      icon: 'fe:git',
      label: 'Git',
      main: false,
      learning: false,
    },
    photoshop: {
      icon: 'simple-icons:adobephotoshop',
      label: 'CSS3',
      main: false,
      learning: false,
    },
    sql: {
      icon: 'simple-icons:mysql',
      label: 'SQL',
      main: true,
      learning: false,
    },
    babel: {
      icon: 'simple-icons:babel',
      label: 'Babel',
      main: false,
      learning: false,
    },
    vue: {
      icon: 'simple-icons:vuejs',
      label: 'Vue',
      main: false,
      learning: false,
    },
    less: {
      icon: 'simple-icons:less',
      label: 'Less',
      main: false,
      learning: false,
    },
    webpack: {
      icon: 'simple-icons:webpack',
      label: 'Webpack',
      main: false,
      learning: false,
    },
    postman: {
      icon: 'simple-icons:postman',
      label: 'Postman',
      main: false,
      learning: false,
    },
    apache: {
      icon: 'cib:apache',
      label: 'Apache',
      main: false,
      learning: false,
    },
    nginx: {
      icon: 'cib:nginx',
      label: 'Nginx',
      main: false,
      learning: false,
    },
  },
}

const projects = {
  alternativa: {
    title: 'Dashboard',
    type: 'Comercial',
    description: 'Dashboard para autonomia de pedidos de clientes, gerenciamento de pedidos.',
    technology: ['js', 'html5', 'css3', 'laravel', 'php8', 'mysql'],
    url: 'https://producao.alternativacard.com',
  },
  cypepanel: {
    title: 'Cyberpanel',
    type: 'Pessoal',
    description: 'Serviço open-source para gerenciamento de servidor',
    technology: ['linux', 'litespeed', 'bash'],
    url: 'https://central.wladiveras.com',
  },
  messages: {
    title: 'Whatsapp Tickets',
    type: 'Comercial',
    description: 'Sistema de whatsapp com multi usuarios e controle de tickets',
    technology: ['linux', 'nodejs', 'react', 'REST API'],
    url: 'https://messages.alternativacard.com',
  },
  portfolio: {
    title: 'Portfolio',
    type: 'Pessoal',
    description: 'Portfolio Open-Source feito em VueJS',
    technology: ['linux', 'nodejs', 'react', 'REST API'],
    url: 'https://github.com/wladiveras/Curriculum',
  },
}

const jobs = ref({
  alternativa: {
    title: 'Desenvolvedor FullStack',
    company: 'Alternativa Card',
    description: 'Responsavel pela criação de sites e sistemas, gerenciamento de servidor, gerenciamento de dns, dominios e administração do banco de dados.',
    year: {
      start: 2021,
      end: 0,
    },
    month: {
      start: 'Outubro',
      end: 'Atual',
    },
  },
})
</script>

<template>
  <div class="container mx-auto">
    <div class="flex flex-row flex-wrap py-4">
      <aside-content :data="data" />
      <main role="main" class="content font-sans w-full sm:w-2/3 md:w-3/4 pt-1 px-2">
        <about-me :data="data"></about-me>
        <about-jobs :job="jobs"></about-jobs>
        <about-project :project="projects"></about-project>
      </main>
    </div>
  </div>
  <footer class="mt-auto">
    ...
  </footer>
</template>

<route lang="yaml">
meta:
  layout: main
</route>
