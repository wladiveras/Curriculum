<template>
  <main class="px-4 py-10 text-center text-gray-700 dark:text-gray-200">
    <router-view />
    <Footer />
    <div class="mt-5 mx-auto text-center opacity-25 text-sm">
      [Home Layout]
    </div>
  </main>
</template>

<style>
.block-inline{
  display:block;
}
.hello-world {
  font-size: 20px;
}
.skills-item {
  display: inline-block;
  width: 50px;
  height:50px;
  vertical-align: middle;
  text-align: center;
}
.line-break {
  line-height: 30px;
}
.icon-skill {
  font-size: 40px;
}
.side-header {
  font-size:16px;
  font-weight: bold;
  margin: 50px 10px 10px 0px;
}

.align-center {
  margin-top: 20px;
  text-align: center;
}
.side-link {
  position: relative;
  top: 6px;
  margin-right: 5px;
  font-size: 20px;
}

.side {
  text-align: left;
}
.container {
  font-size: 0.80em;
  background: #ffff;
  border-radius:5px;
  border: #444c56 1px solid;
}

.dark .container {
  background: #22272e;
  border-radius:5px;
  border: #444c56 1px solid;
}
.container {
  max-width: 1100px;
  margin: 0 auto;
}

.content {
  text-align: left;
  padding-top: 10px;
}

.color-default {
  color: rgba(99,179,237,1);
}
.dark .color-default {
  color: rgba(99,179,237, 1);
}
.content-icon {
  margin: 5px 0px 5px 0px;
  width:24px;
  height:24px;
}

.avatar {
  border-radius: 10px;
  margin: 0 auto;
}
.zoom {
  transition: transform .2s;
}

.zoom:hover {
  transform: scale(1.5);
}
</style>
