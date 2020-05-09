# Demo example

1. Start the server
2. Got to `http://localhost:3000/posts-without/`
3. Click on "Nuxt" in the Navbar above
4. Click on "Vue" in the Navbar above
5. You don't see any transitions happening
6. Now change your URL to  `http://localhost:3000/posts/`
7. Same procedure, click on "Nuxt"
8. Click on "Vue"
9. You see the fade transition happening thanks to the other layout (`with-key.vue`)


The nuxt-child-key is interesting for transitions that should directly affect the whole NuxtChild component or wrappers,
e.g. when using page-level tabs
