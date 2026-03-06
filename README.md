<div align="center">

<pre>
 ┌────────────────────────────────────────────────────┐
 │  user@dev:~/projects$ ./recipe                     │
 │                                                    │
 │        ██████╗   █████╗   ██╗  ██╗  ███████╗       │
 │       ██╔════╝  ██╔══██╗  ██║ ██╔╝  ██╔════╝       │
 │       ██║       ███████║  █████╔╝   █████╗         │
 │       ██║       ██╔══██║  ██╔═██╗   ██╔══╝         │
 │       ╚██████╗  ██║  ██║  ██║  ██╗  ███████╗       │
 │        ╚═════╝  ╚═╝  ╚═╝  ╚═╝  ╚═╝  ╚══════╝       │
 │                                                    │
 │  > coffee cupcake recipe page · html + css         │
 └────────────────────────────────────────────────────┘
</pre>

![type](https://img.shields.io/badge/type-static%20page-2ea043?style=for-the-badge&labelColor=0d1117)
![version](https://img.shields.io/badge/version-1.0.0-58a6ff?style=for-the-badge&labelColor=0d1117)
![license](https://img.shields.io/badge/license-mit-8b949e?style=for-the-badge&labelColor=0d1117)
![stack](https://img.shields.io/badge/stack-html%20%2B%20css-d29922?style=for-the-badge&labelColor=0d1117)

</div>

---

## `$ cat about.txt`

```
recipe is a one-page site for a coffee cupcake: coffee and chocolate
batter, a condensed-milk coffee filling, whipped cream on top.

there is no javascript, no build step and no images. index.html holds
three sections (about, ingredients, preparation); style.css lays them
out as one 800px cream card, set in the Alice serif, over a solid
brown page.

built as a hands-on study of html and css, turning a figma layout into
a page — the page text itself is in portuguese.
```

## `$ ls features/`

```
[x] one static page: html + one stylesheet, no javascript, no build
[x] about block with time (1h10), yield (12 servings) and difficulty
[x] 14 ingredients and a three-part method: cake, filling, assembly
[x] 800px cream card with rounded corners on a #573a37 brown page
[x] Alice serif from google fonts on a brown-on-cream palette
[x] footer credit with a ♥ character in the card color, under the card
[x] published on github pages at miguelcrwz.github.io/recipe
[ ] fixed 800px width, no media queries: scrolls sideways on a phone
[ ] flat ingredient list: soluble coffee and chocolate powder repeat
[ ] the method is one <p> split by <br />, not numbered steps
[ ] no favicon, portuguese only, one recipe hardcoded, no tests
```

## `$ cat stack.lock`

```
runtime     any modern browser
framework   none — plain html + css, no javascript
markup      html5, one page (lang="pt-br")
styling     plain css, one stylesheet, no preprocessor
fonts       Alice from google fonts (needs network, falls back to serif)
infra       github pages, publishes main as-is
tests       none yet
tooling     figma for the layout, python http.server to preview
```

## `$ ./install.sh`

```bash
# clone
git clone https://github.com/miguelcrwz/recipe.git
cd recipe

# dependencies (none — plain html + css; python 3 only serves it locally)
python --version
```

## `$ ./run`

```bash
# development (from the repo root)
# then open http://localhost:8000 — python3 on linux / macos
python -m http.server 8000

# production (github pages publishes main as-is)
#   https://miguelcrwz.github.io/recipe/
git push origin main
```

```
Serving HTTP on :: port 8000 (http://[::]:8000/) ...
::1 - - [20/Feb/2026 08:31:12] "GET / HTTP/1.1" 200 -
::1 - - [20/Feb/2026 08:31:12] "GET /style.css HTTP/1.1" 200 -
::1 - - [20/Feb/2026 08:31:13] code 404, message File not found
::1 - - [20/Feb/2026 08:31:13] "GET /favicon.ico HTTP/1.1" 404 -
```

## `$ describe index.html`

```
#page          div       the 800px cream card that wraps the recipe
#about         section   h1, intro, time / yield / difficulty
#ingredients   section   ul with 14 items for cake, filling and topping
#preparation   section   one p, three parts split by <br /><br />
footer         footer    outside the card: "Feito com ♥ pelo Miguel"
```

## `$ tree`

```
recipe/
├── index.html   # about, ingredients, preparation, footer
├── style.css    # palette, Alice font, 800px card, footer
├── .gitignore
├── LICENSE
└── README.md
```

## `$ git log --oneline roadmap`

```
a1b2c3d  swap the fixed 800px width for max-width and a phone breakpoint
e4f5g6h  split the ingredients into cake, filling and topping lists
i7j8k9l  turn the method into an ordered list of steps
m0n1o2p  add a favicon and an english version of the page
```

## `$ cat LICENSE | head -1`

```
MIT © 2026 Miguel Cruz
```

## `$ whoami`

```
miguel cruz
├── github    https://github.com/miguelcrwz
├── linkedin  https://linkedin.com/in/miguelcrwz
└── email     miguwlcrwz@gmail.com
```

<div align="center">

<pre>
$ exit
[process exited with code 0]
</pre>

</div>
