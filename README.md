### Guide

This is a template project for doing a presentation with reveal.js

You can clone this repository or create your own from scratch using guide below

### Generate from Scratch

To generate from scratch follow these steps

```
npm install -D @webpack-cli/generators
npx webpack-cli init
```

From the options that come up (options may change in future versions)

```
? Which of the following JS solutions do you want to use? Typescript
? Do you want to use webpack-dev-server? Yes
? Do you want to simplify the creation of HTML files for your bundle? Yes
? Do you want to add PWA support? No
? Which of the following CSS solutions do you want to use? CSS only
? Will you be using PostCSS in your project? No
? Do you want to extract CSS for every file? No
? Do you like to install prettier to format generated configuration? Yes
? Pick a package manager: npm
```


```
npm i --save-dev @types/reveal reveal.js
```


Add the following to tsconfig.json

```
    "noImplicitAny": false,
    "moduleResolution": "node",
    "typeRoots": [
      "./node_modules/@types"
    ],
```


You will need a html file with the following in the body

```
<div class="reveal">
    <div class="slides">
        <section>
            <h1>Hello World!</h1>
        </section>
    </div>
</div>
```

You will need the index.ts file with

```
import Reveal from "reveal.js"
import Markdown from 'reveal.js/plugin/markdown/markdown.esm.js';

import "reveal.js/dist/reveal.css"
import "reveal.js/dist/theme/black.css"

let reveal = new Reveal({
    plugins: [ Markdown ]
})
reveal.initialize()
```



Start the server

```
npm run serve
```
