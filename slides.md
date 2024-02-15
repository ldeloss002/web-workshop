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

An introduction to web development for all skill levels.

<!--
  My name is Lemuel, I am also a student here, and I'm here to teach you about web development.
 -->


---
---

<div class="flex items-center justify-between">

  ![Screenshot](/screenshot.png){class="pr-30"}

  <box v-click class="grid text-6xl grid-cols-2 border-purple bg-purple bg-opacity-20 my-20 mx-auto">
    <logos-html-5 :class="['rotate-20', { 'animate-zoom-in-left': $clicks > 0 }]" />
    <logos-css-3 :class="['rotate--15', { 'animate-zoom-in-right': $clicks > 0 }]" />
    <logos-javascript :class="['rotate--20 [grid-column:1/-1]', { 'animate-zoom-in-up': $clicks > 0 }]" />
  </box>
</div>

<!--
  We'll be making a TODO app, a website that lets you add, remove, and complete tasks that you have to do._**[>]**_

  We'll be using HTML, CSS, and JavaScript to build it.
  Having three whole languages to learn for one website is a bit much, but it's not as complicated as it sounds.
 -->

---

<game-icons-grab
  v-click="1"
  :class="[
    'absolute', 'top-15', 'left-15', 'text-9xl', 'text-[#9394d2]',
    { 'animate-tada': $clicks > 0, 'opacity-20': $clicks > 2 }
  ]"
/>
<arrow v-click="2" x1="375" y1="300" x2="600" y2="300" width="5" />

<div
  v-click="1"
  :class="[
    'flex', 'justify-around', 'text-6xl', 'absolute' ,'w-full' ,'top-30', 'left-0', 'transition-opacity',
    { 'opacity-20': $clicks > 2 }
  ]"
>
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
  There are actually a lot of different ways to build websites, and a lot of different tools to use.

  Most of "Big Tech"_**[>]**_  and all the companies you know are using "frameworks and libraries"
  to build their websites, that makes some of the more complicated stuff easier to do.

  "frameworks and libraries" just means using some *other* languages or someone else's code to build a website.
  The thing about developing on the web, is whatever you use will all eventually get _**[>]**_ converted back into HTML, CSS, and JavaScript.

  It's like using a _**[>]**_ GPS instead of a traditional map, and it can a good thing because it lets you *focus* on more important things than the details.
  But sometimes, you need to know how to use a map, in case the GPS fails to tell you how to get somewhere very specific or obscure.

  In case the analogy didn't stick, we're learning HTML, CSS, and JavaScript so you can better understand what websites are made of, and how a framework might be used to make them.

  But first, a poll:

  - How many of you have no experience in web development?
  - How many of you have some experience in web development?
  - Beginner, Intermediate, Advanced?
 -->

---
layout: center
---

<https://bit.ly/ccny-web-workshop>{class="text-4xl font-bold"}

<!--
  I've set up a template to use that has basic the functions for adding, removing, and completing tasks.

  [WAIT]

  I'll be explaining the how the existing code works, but I'll help you learn to style the your version of the website
  on your own.
  I also want you decide with me what new features we should add in the end, and maybe how you think we should implement them.

  [WAIT]

  Im going to go through a lot of the code, but only be explaining the details that are important now.
  Feel free to ask questions at literally any time, but we should have some time at the end for questions too.
 -->

---
layout: two-cols
---

```html {all|2|12|3|8|9|11|all|6|7|4|all|3-8}{lines: true}
<!DOCTYPE html>
<html>
    <head>
        <title>TODO</title>

        <link rel="stylesheet" href="styles.css" />
        <script type="module" src="script.js"></script>
    </head>
    <body>
        ...
    </body>
</html>
```

<tag v-click name="html" class="w-sm">
  <tag name="head">
    <tag name="title">TODO</tag>
    <tag name="link" />
    <tag name="script" />
  </tag>
  <tag name="body">...</tag>
</tag>

<!--
  This is part of the template `index.html` file that you should be starting with.

  Except for the `...` part, that's just me cutting out the rest.

  HTML is used to write the structure of your website, and it is made up of "tags".

  Tags are used to structure content, they have a start and end, and can have attributes. Tag can also have other tags inside them... but not all.

  You can see the start and end tags for the `html`_**[>>]**_, `head`_**[>>]**_, and `body`_**[>>]**_ tags.

  _**[>]**_

  There are *self*-closing tags, like the _**[>]**_ `link` tag, which is used to *link* to an outside file, in this case, our `styles.css`.
  Then there's _**[>]**_ `script` tag specifically to load JavaScript, in this case, our `script.js` file.

  There's also the _**[>]**_ `title` tag is used to set the title of the website, which is what you see in the tab of your browser on the top when you visit a website.

  _**[>]**_

  The `rel=`, `href=`, `type=`, and `src=` are all attributes, and are used to attribute additional information about a tag.

  _**[>]**_

  Tags have a parent-child relationship, and in this case, the `head` tag is the parent of its children: `title`, `link`, and `script`.

  Yeah, they're technically all single parents, that's just the terminology.

  It helps to think of this code like the diagram on the right, where all the tags are nested inside each other.

  And all the tags here so far in the `head` tag.

  _**[>]**_

  All the stuff in the `head` tag is not actually what's **visible** on the website, but instead provides information *about* the website, like the title, and links to other files.
 -->

---

```html {6-24|7,10|8|9|12|14,23|15,22|16,19|17|18|21|all|15-22}{lines: true}
<!DOCTYPE html>
<html>
    <head>
      ...
    </head>
    <body>
        <div>
            <input id="text-input" placeholder="What to do..." />
            <button id="add-button" type="submit">Add</button>
        </div>

        <ul id="todo-list"></ul>

        <template id="todo-item-template">
            <li class="todo-item">
                <label class="todo-item-label">
                    <input class="todo-item-checkbox" type="checkbox" />
                    <span class="todo-item-content"></span>
                </label>

                <button class="remove-button">Remove</button>
            </li>
        </template>
    </body>
</html>
```

<!--
  The `body` tag is where all the REAL content of the website goes. So, here's the rundown:

  - The _**[>]**_ `div` tag is used to group other tags together. Here it's used to group the input and button.
  - The _**[>]**_ `input` tag here is used to get written text from the user.
  - The _**[>]**_ `button` tag is a button. You can click it.
  - The _**[>]**_ `ul` tag is for unordered lists, it's empty for now, but we'll use it to store our tasks.
  - The _**[>]**_ `template` tag is not visible on the website, it's used to store tag information that we can make copies of later.
  - The _**[>]**_ `li` tag is for list items.
  - The _**[>]**_ `label` tag is used to create a label for `input` tag with text.
  - The _**[>]**_ `input` tag here is also used to create a checkbox, the `input` tag is used for a lot of things.
  - The _**[>]**_ `span` tag is just used to structure text. It's empty, but you'll see why later.
  - _**[>]**_ Another button.

  _**[>]**_

  It's a lot of tags, but most of them are just for semantics which are important for
  accessibility, search engines, and not getting yelled at by your coworkers for only using `div` all the time.

  You can see that all tags here either have an `id` or `class` *attribute*.

  The `id` attribute is used to identify one specific tag, that is unique. No more than one tag can have the same id.
  The `class` attribute is used to categorize tags, meaning and multiple tags can have the same class.

  The only tags using classes are the tags inside the _**[>]**_ `template` tag, and that's because we'll be making copies of them later, so, there *would* be multiple of them.

  `id` and `class` attributes are used for *selectors* (that's our word of the day), which are used in both CSS and JavaScript to select one or more tag from our HTML.
  -->

---
layout: two-cols
---

```css {15-34|15,20|22,27|29,35|15-35}{lines: true, startLine: 13}
...

label {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
}

#todo-list {
    padding: 0;
    list-style-type: none;
    width: 100%;
    max-width: 30rem;
}

.todo-item {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 1rem;
    padding: 0.5rem;
}

...
```

<v-after>

  ![Screenshot](/inspect.png){class="w-100"}

</v-after>

<!--
  This is some of the CSS that's in the `styles.css` file.

  CSS is used to style the website. It looks *very* different from HTML, but it's not that hard to understand.

  We start with a query selector, and then add *properties* to change the look of the tags that are selected.

  Here, we have three kinds of selectors being used, the tag selector, the id selector, and the class selector.

  The _**[>]**_ tag selector is used to select all tags of a certain type, and here it's used to select all `label` tags.

  The _**[>]**_ id selector, starts with a `#`, and used to select the one and only one tag with the id `todo-list`.
  In this case, it's used to select the `ul` tag.

  The _**[>]**_ class selector, starts with a `.`, and is used to select all tags with the class `todo-item`.
  In this case, it's used to select all our `li` tags with the class `todo-item`.

  _**[>]**_

  This image is a screenshot of a browser's developer tools. I can inspect the website, and see all kinds of information about it.
  This is a more styled version of the website that you're using, but it's technically the same HTML right now.

  Here I've selected `li.todo-item`, which is the `li` tag with the class `todo-item`.
  Don't mind that it's inside the `ul`, but do mind that how `ul` has the `todo-list` id, and shown with the `ul#todo-list`.

  I won't go into details about the CSS properties *yet*, as we'll worry about how the website works first, then we can make it look nice.
 -->

---
layout: two-cols
---

```js {all|1-4|2,9,21|2,9-21|6|1-2,6,9-14,21|1-2,6,9-17,21|1-2,6-7,9-17,21|1-2,6-7,9-20,21}{lines: true}
let textInput = document.querySelector("#text-input");
let addButton = document.querySelector("#add-button");
let todoList = document.querySelector("#todo-list");
let todoItemTemplate = document.querySelector("#todo-item-template");

let state = [];
loadState();

addButton.addEventListener("click", function() {
  let task = {
    id: Date.now(),
    content: textInput.value,
    checked: false
  };

  state.push(task);
  saveState();

  let todoItem = createItemElement(task);
  todoList.append(todoItem);
});

// ...
```

<div class="flex flex-col gap-2 items-center">
  <div v-click="3" :class="['flex', 'flex-col', 'gap-4', 'items-center', { 'opacity-50': $clicks > 6 }]">
    <pre><code
      v-html="'state = ' + (
        $clicks < 5 ? '[\n\t...\n]' : `[\n\t{\n\t\tid: ${Date.now()},\n\t\tcontent: ...,\n\t\tchecked: false\n\t}\n]
      `)"
    /></pre>
  </div>

  <div :class="['flex', 'flex-col', 'gap-4', 'items-center', { 'opacity-50': $clicks > 2 && $clicks < 7 }]">
    <prompt v-click="1" :add-class="{ 'animate-heart-beat': $clicks > 0 }" />
    <task v-click="2" />
    <task v-click="7" />
  </div>
</div>

<!--
  This is some of the JavaScript that's in the `script.js` file.

  Once again, a very different looking language.

  The first four lines are using the same selectors we saw earlier, to get the tags we want from our HTML, so that we can use it here in JavaScript.
  `#text-input` to get our input tag with id `text-input`, `#add-button` to get our button tag with id `add-button`, and so on.

  Using our `addButton`, we add an *event listener* to the button, just meaning that when it's clicked, some function runs.
  This function, in the end, adds a new task to our state, and then adds it to our website.

  "State" in programming just means the current condition of something, nothing but terminology.

  Our "state" here is a list. It's a that stores all our tasks, and it's used to keep track of what tasks are added, removed, and completed.
  Each task is some object that has an id, some content, and a 'checked' property.

  The id is used to uniquely identify the task, and uses the `Date.now()` function to set the current time in milliseconds as the id.
  The content is the text of the task, it gets it from our input tag by using the `value` property of the our `textInput` variable.
  The checked property is used to keep track of whether the task is completed or not, and is set to `false` by default.

  After the task is created, it's added to the `state` list, and then saved to the browser's local storage.
  So, if you refresh the page, all the tasks and their states are still there.

  In fact, the `loadState` function runs when the website starts, and it's used to load the state from the local storage.

  The `createItemElement` function turns the task object into an HTML element, and then it's added to the `todoList` tag using the `append` function.
  I'm going to be using "element" and "tag" interchangeably from now on.

  Notice, there are two separate things being changed here, the state and the website, and they're updated separately.
 -->


---
layout: two-cols
---

```js {all|27-29|31-32|34-39|41-49|51}{lines: true, startLine: 26}
function createItemElement(item) {
    let todoItemTemplate = document.querySelector("#todo-item-template");
    let todoItem = todoItemTemplate.content.cloneNode(true);
    let listItem = todoItem.firstElementChild;

    let content = todoItem.querySelector(".todo-item-content");
    content.textContent = item.content;

    let checkbox = todoItem.querySelector(".todo-item-checkbox");
    checkbox.checked = item.checked;
    checkbox.addEventListener("input", function() {
        item.checked = checkbox.checked;
        saveState();
    });

    let removeButton = todoItem.querySelector(".remove-button");
    removeButton.addEventListener("click", function() {
        state = state.filter(function(listItem) {
            return listItem.id !== item.id;
        });
        saveState();

        listItem.remove();
    });

    return todoItem;
}
```

<div class="flex flex-col gap-12 items-center">
  <pre v-if="$clicks < 5"><code
    v-html="`item = {\n\tid: ${Date.now()},\n\tcontent: ...,\n\tchecked: false\n}`"
  /></pre>

  <task class="border-dashed border-3 border-purple opacity-50" content-class="invisible" v-if="$clicks < 5" />

  <prompt v-if="$clicks > 4" />
  <task v-if="$clicks > 4" />
  <task v-if="$clicks > 4" />

  <div class="flex flex-col gap-12 items-center">
    <task
      v-click="1"
      :class="{ 'animate-zoom-in-down': $clicks > 0 }"
      :checkbox-class="{ 'animate-shake-y': $clicks > 2 }"
      :content-class="$clicks > 1 ? 'opacity-100' : 'opacity-0'"
      :remove-class="{ 'animate-tada': $clicks > 3 }"
    />
  </div>
</div>

---
layout: center
---

<https://bit.ly/ccny-web-workshop>{class="text-4xl font-bold"}

---
layout: center
---

<box class="flex flex-col relative p-4 gap-2 bg-green b-green bg-op-20 w-150 h-full items-center">

  ![BYTE Logo](/byte.jpg){class="absolute top--10 right--25 w-50 rounded-full"}

  <div class="text-4xl font-bold w-80">ACM B.Y.T.E 2024 Spring Cohort</div>

  ![BYTE QR Code](/byte-qrcode.png){class="h-50 bg-white p-2 rounded-3"}

  <https://forms.gle/th9v24PAdPQYtPd4A>
</box>

<!--
  B.Y.T.E stands for Build Your Technical Experience.

  Together with the guidance of an experienced board, you as a member of BYTE will build software with your peers. We want you to develop team work and project planning skills, and be provided with supervision and a sense of community. Giving you the confidence to build applications outside of your CCNY education.

  By participating, you will gain experience in which field of software engineering you want to pursue (i.e. data science, backend, etc.). This exposure is invaluable to your development as a software engineer and for your resume. If this is what you're looking for in your career, please consider applying!
 -->

---
layout: center
---

<box class="relative flex flex-col p-4 bg-blue b-blue bg-op-20 w-150 h-full items-center justify-center">

  ![GWC Logo](/gwc.png){class="absolute top--10 right--23 w-50"}

  <div class="text-4xl font-bold w-80">Girls Who Code Club Discord</div>

  ![GWC QR Code](/gwc-qrcode.png){class="h-50 bg-white p-4 rounded-3"}

  <https://tinyurl.com/ccnygwc>

</box>

<!--
  Join the Mentoring Corps: mentor high school students. 3-5 hour commitment per month. No prior coding experience required. About $400 for the semester. Join our Girl's Who Code club discord and let us know you would like to participate!

  6/313 is the Girls Who Code club's official club room for the spring semester. You can stop by any Thursday between 12:30 to 2 PM to chill and make friends!
 -->

---
layout: center
---

  ![Headstarter](/headstarter.jpg){class="h-120"}
