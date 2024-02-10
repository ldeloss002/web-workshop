---
# background: https://source.unsplash.com/collection/94734566/1920x1080
# class: text-center
highlighter: shiki
# lineNumbers: false
info: |
  Web Workshop for Beavers Code (ACM @ CCNY) club.
  Introduction to web development and how to get started.
drawings:
  persist: false
fonts:
  # sans: Lato
  # sans: Raleway
  serif: Libre Baskerville
transition: slide-left
title: Web Workshop
mdc: true
---

Welcome to **GWC** + **Beavers Code (ACM @ CCNY)**

# Web Workshop

<!--
  My name is Lemuel, I am also a student at CCNY, and have been in the space of web development for a while now (almost half my life [help me]).

  And like most online tech spaces, everything is *always* changing, and it feels important to keep up with the latest trends and technologies.
  It's important to know what's out there and what's possible, but it's also good to stick with what you know if it works for you.
 -->


---
clicks: 1
---

# What we'll be Making

<box v-click class="grid text-6xl grid-cols-2 border-purple bg-purple bg-opacity-20 my-20 mx-auto">
  <logos-html-5 :class="['rotate-20', { 'animate-zoom-in-left': $clicks > 0 }]" />
  <logos-css-3 :class="['rotate--15', { 'animate-zoom-in-right': $clicks > 0 }]" />
  <logos-javascript :class="['rotate--20 [grid-column:1/-1]', { 'animate-zoom-in-up': $clicks > 0 }]" />
</box>

<!--
  We'll be making a TODO app, a website that lets you add, remove, edit, and complete tasks.

  To do this, we'll learn about HTML, CSS, and JavaScript, and how they work together to create a website.
 -->

---
clicks: 3
---

# What we'll Learn

<game-icons-grab
  v-click="1"
  :class="[
      'absolute', 'top-15', 'left-15', 'text-9xl', 'text-[#9394d2]',
      { 'animate-tada': $clicks > 0, 'opacity-20': $clicks > 2 }
    ]"
  />
<arrow v-click="2" x1="375" y1="300" x2="600" y2="300" width="5" />

<div v-click="1" :class="['flex', 'justify-around', 'text-6xl', 'absolute' ,'w-full' ,'top-30', 'left-0', 'transition-opacity', { 'opacity-20': $clicks > 2 }]">
  <box class="grid grid-cols-2 border-purple bg-purple bg-opacity-20">
    <logos-vue class="rotate-20" />
    <logos-react class="rotate-15" />
    <logos-solidjs-icon class="rotate--20" />
    <logos-angular-icon class="rotate--15" />
  </box>

  <box v-click="2" class="grid grid-cols-2 border-purple bg-purple bg-opacity-20">
    <logos-html-5 class="rotate-20" />
    <logos-css-3 class=" rotate--15" />
    <logos-javascript class="rotate--20 [grid-column:1/-1]" />
  </box>
</div>

<div v-click="3" class="flex justify-around text-8xl absolute w-full top-60 left-0">
  <box class="flex flex-col border-blue bg-blue bg-opacity-20">
    <icon-park-gps class="rotate--20" />
    <span class="text-2xl">GPS</span>
  </box>

  <box class="flex flex-col border-blue bg-blue bg-opacity-20">
    <icon-park-map-draw class="rotate-20" />
    <span class="text-2xl">MAP</span>
  </box>
</div>

<!--
   Most of "Big Tech" and all the companies you know are using a **framework** or **library** to build their websites, that makes the complicated stuff easier to do.

  Whatever they use, it all eventually get converted into HTML, CSS, and JavaScript.

  Think of it like using a GPS instead of a traditional map, and it's a good thing because it lets you focus on more important things.

  In the same analogy, today you'll learn how the GPS works, so you can understand how to use the map better.
 -->


---

# Structure

```html {all|3-7|8-13}
<!DOCTYPE html>
<html>
  <head>
    <title>TODO</title>

    <link rel="stylesheet" href="css/main.css" />
    <script src="./script.js"></script>
  </head>
  <body>
    ...
  </body>
</html>
```

---



---

# Behavior

<!--
  I'm going to start using JavaScript by talking about the control flow of what we want our website to do, rather than the means of how we're going to do it.
 -->

<!--
  So, what was the point of having an intermediate state between our HTML and JavaScript?
 -->

 <!--
  Why render everything all over again?

  Operations such as removing, editing, and checking if a task is completed, all require DOM manipulation, and that means, so does our load function.


  -->


---

# The Render Loop

<!--
  So, the render loop is kinda bad, because it's not efficient, and it's not scalable.
   -->
