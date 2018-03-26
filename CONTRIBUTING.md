# Contribución

Con tu ayuda, podemos crear una herramienta de referencia de facil entendimiento que ayude a miles de personas que deseen aprender código en los siguientes años.  💛

> La siguiente tabla de contenido fue generada automaticamente usando [Markdown TOC](https://marketplace.visualstudio.com/items?itemName=AlanWalk.markdown-toc) con la extención en  [VS Code](https://code.visualstudio.com/).

<!-- TOC -->

- [Contribución](#contributing)
  - [Pasos](#Pasos)
  - [Creando un PR](#creating-a-pr)
    - [Usando GitHub.com](#using-githubcom)
    - [Clonación local](#cloning-locally)
    - [Ejecutando localmente](#running-locally)
  - [Obtener PR Accepted](#getting-pr-accepted)
    - [Etiquetas](#labels)
    - [Confligtos/Contenido Duplicado](#conflictingduplicate-content)
    - [Solicitud de cambios](#requesting-changes)
    - [Compilación Travis CI](#travis-ci-build)
    - [Cierre](#closing)
    - [Ayuda](#getting-help)
  - [Articulo guias de estilo](#article-style-guide)
    - [Titulo](#title)
    - [Modularidad](#modularity)
    - [Bloques de Código](#code-blocks)
    - [Enlaces](#links)
    - [Imagenes](#images)
    - [Atribuciones](#attributions)
    - [Recursos](#resources)
    - [Formatos](#formatting)
  - [Tecnicas de escritura](#technical-writing)
    - [Resumen](#outline)
    - [Introducción](#intro)
    - [Contenido](#content)
    - [Claridad](#clarity)
    - [Voz](#voice)
      - [Pasivo](#passive)
      - [Activo](#active)
    - [Puntos de Vista](#point-of-view)
    - [Abreviaciones](#abbreviations)
    - [Nombres propios](#proper-nouns)
    - [Herramientas de terceros](#third-party-tools)
- [Revisando PRs](#reviewing-prs)
  - [Funcionar y mezclar](#squash-and-merge)
  - [Filtado de PRs](#filtering-prs)
  - [Plantillas](#templates)
    - [Error de compilación](#build-error)
    - [Sincronización de bifurcaciones](#syncing-fork)
    - [Mezclando conflictos](#merge-conflicts)
    - [Duplicidad](#duplicate)
    - [Cierre](#closing-1)

<!-- /TOC -->

## Pasos

1. 🍴 [Darle Fork este repositorio](https://github.com/freeCodeCamp/guides#fork-destination-box)
2. 👀️ Siga las guias de contribución resumidas a continuación.
3. 🔧 ¡Has cambios increibles!
4. 👉 [Crea una petición "pull"](https://github.com/freeCodeCamp/guides/compare)
5. 🎉 ¡Haz que tu petición sea aprovada - Exito!

O simplemente [reporta un problema ](https://github.com/freeCodeCamp/guides/issues) - toda la ayuda cuenta!

## Creando un PR

### Usando GitHub.com

Ve el video demostrativo o siguie los siguientes pasos:

![GIF mostrando los pasos de GitHub](https://i.imgur.com/0cmxJwN.gif)

1. Ve al folder de **"pages"**  (localizado en `guides/src`) y encuentra el articulo plantilla que quisieras escribir o editar.

    > Todas las plantillas estaran en un documento index.md 

2. Presiona el icono de lapiz con <kbd>Edit this article</kbd>  y hazle cambios al archivo en formato Markdown de GitHub.

3. Ve hasta el fondo de la pantalla y agrega un mensaje de commit explicando tus cambios.

4. Despues selecciona la opcion radio button que dice  **"Create a new branch for this commit and start a pull request"** y presiona <kbd>Propose file changes</kbd>.

5. En la siguiete pantalla, podras agregar cualquier detalle acerca de tu PR y despues dar clic en <kbd>Create pull request</kbd>.

### Clonar localmente

1. Hazle Fork a este repositorio

2. Copialo a tu maquina local con el siguiente comando:

    ```bash
    git clone https://github.com/bigdatamx/guides-capacitacion-praxis.git
    ```

3. Agrega un upstream remoto de forma que git sepa en donde se encuentra la guia oficial de BigdataMx con el siguiente comando:

    ```bash
    git remote add upstream https://github.com/bigdatamx/guides-capacitacion-praxis.git
    ```

4. Crea un nuevo branch para tu trabajo con el siguiente comando `git checkout -b NOMBRE-BRANCH`.

    > Intenta ponerle un nombre que describa el topico de tu articulo como `fix/articulo-html`

5. Escribe tu articulo, hazle commit a tus cambios locales y sañe úsh a tu nuevo branch en GitHub con el comando `git push origin NOMBRE-BRANCH`

6. Ve a tu respositorio en GitHub y abre un PR 

Asegurate de mantener un fork local en crecimiento de forma que se mantenga actualizado con el repositorio  de BigdataMx.

La proxima vez que quieras contribuir, hazle checkout a tu branch local `master` y corre el comando `git pull --rebase upstream master` antes de crear un nuevo branch.

Esto tomará todos los cambios en el `master` original sin hacer un commit adicional en tu repositorio local.

### Correrlo local

```bash
# Asegurate de tener yarn instalado
npm install -g yarn

# dale fork tu repo

# clona tu  repo
git clone https://github.com/YOUR-GITHUB-USERNAME/guides.git

# posicionate en la raiz de el repo
cd guides

# instala las dependencias
yarn install

# correlo localmente
yarn run dev
```

Usamos `yarn` porque `netlify` compila el sitio con `yarn`.

## tu PR aprovada

Aqui hay una guia que siguen los revisores de contenido para los PR:


Here are a few guidelines the reviewers follow when reviewing PRs:
- La descripcion y el titulo son relevantes
- La PR respeta el [guia de estilo de articulo](./CONTRIBUTING.md/#article-style-guide)
- Sigue los tips generales  encontrados en [Guia de moderador](https://forum.freecodecamp.org/t/freecodecamp-moderator-guidelines/18295)
- Con que el pull request mejore o expanda la guia, lo aceptamos aunque contenga errores de sintaxis en Español o en el contenido parcial.
- Pull request viejos son revisados primero

### Etiquetas

- **content** es para pull request que modifican el contenido de los articulos en la guia (agregan un nuevo articulo o actualizan un articulo existente)
- **duplicate** es para pull requests que tienen el mismo contenido que en otro PR abierto
- **changes requested** es para pull request que necesitan un cambio antes de ser aceptadas
- **stale** es para pull requests con la etiqueta _"changes requested"_ que no tienen actividad por mas de 2 semanas y subsqcuentemente seran cerrados.
  - las _stale_ pull request deben de estar cerradas.
  - Aqui hay [un ejemplo](https://github.com/freeCodeCamp/guides/pull/235).

### Contenido Duplicado/Conflictivo

Una PR es considerada un **Duplicado** si le hace cambios al mismo articulo con una PR diferente.

En general, un revsor deberá:

1. Ordenar las PR por la mas vieja
2. Buscar PR con contenido similar
3. Combinar la PR mas nueva con la mas vieja

Es muy probable que existan conflictor al combinar PRs duplicadas.

Los revisores harán un esfuerzo a resolver estos conflios en la combinación de PRs.

### Pedir cambios

Si una pull request no es perfecta, el revisor podrá:
- pedir cambios al contribuidor y agregar la etiqueta *cambios pedidos*
- Arreglar cambios menores y hacer un commit sobre la PR

### Compilacion Travis CI 
Todas las PRs deben de pasar la verificación de Travis CI antes de que podamos combinarlos.

Si una PR rompe la compilación (Travis CI mostrara una "X" roja) habra dos tipos de soluciones.

Deberas de arreglar el problema antes de que combinemos tu PR:

1. Tu PR crea un nuevo articulo y le falta el `index.md` de alguna forma.
    - Cada folder dentro de  `src/pages` necesita un archivo`index.md` dentro de el (y el nombre debe de ser `index.md`).
    - Dos escenarios probables son:
      - nombraste el archivo con algo diferente a`index.md`, o
      - creaste un nuevo folder y despues un sub-folder, y escribiste el articulo en el subfolder pero no pusiste el archivo `index.md` en el nuevo folder.
2. El articilo no tiene un `title` en la cabezera.
    - Por favor checa el [Title](#title) en la seccion dentro de [guia de diseño de articulo](#article-style-guide).

### Closing

We close a pull request

- if an older PR for the same article is merged, and your PR doesn't add new content
- if there is zero/little effort in it (e.g: copy pasting from another source like Wikipedia)
- if there is copied text from a copyrighted source - see [Citation issue](https://github.com/freeCodeCamp/guides/issues/2503)
- if it does not respect the [Article Style Guide](#article-style-guide)
- if it does not respect the [Academic Honesty policy](https://www.freecodecamp.org/academic-honesty)
- if it is stale (if a change is requested and there is no activity for about 2 weeks)

Also, if you're working off a "stub" article, your changes must be substantial enough to replace the stub text.

We won't accept a PR that only adds links to the "More Information:" section.

The repository has a `Normalise.js` script that adds attributes to links, but also checks for "This is a stub..." text via a RegEx.

If found, it will revert the article text back to the generic stub text (and erase your changes).

This is intended behavior, since it allows us to update all stubs if the template stub changed for any reason.

### Getting Help

There's a community of support from a whole team of contributors, whom you can bounce ideas off of and ask for input on your writing.

Stay active in the [contributors chat room](https://gitter.im/freecodecamp/contributors) and ask lots of questions.

## Article Style Guide

We've written the following guide to writing Guide articles to help you get started contributing.

### Title

Article titles should be as short, concise, and to-the-point as possible.

We want campers to quickly find the information they're looking for, and the title should reflect the main theme of the article.

Folder name is used in the URL, so only use dashes -, numbers 0-9, and lowercase letters a-z for it.

However, you can include special characters in the article title.

Here are some examples of properly named titles:

> [`src/pages/html/tables/index.html`](https://github.com/freeCodeCamp/guides/blob/master/src/pages/html/tables/index.md)

```markdown
---
title: Tables
---
```

> [`src/pages/css/borders/index.md`](https://github.com/freeCodeCamp/guides/blob/master/src/pages/css/borders/index.md)

```markdown
---
title: Borders
---
```

> [`src/pages/javascript/loops/for-loop/index.md`](https://github.com/freeCodeCamp/guides/blob/master/src/pages/javascript/loops/for-loop/index.md)

```markdown
---
title: For Loop
---
```

### Modularity

Each article should explain exactly one concept, and that concept should be apparent from the article's title.

We can reference other articles by linking to them inline, or in an "Other Resources" section at the end of the article.

Our goal is to have thousands of articles that cover a broad range of technical topics.

### Code Blocks

Campers will likely use Guide articles as a quick reference to look up syntax. Articles should have simple real-world examples that show common-use cases of that syntax.

GitHub-flavored markdown supports [syntax highlighting in code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/#syntax-highlighting) for many programming languages.

To use it, indicate the language after ```.

For example, the following Markdown

```markdown
    ```html
    <div class='awesome' id='more-awesome'>
      <p>This is text in html</p>
    </div>
    ```
```

will output the following code block with `HTML` syntax highlighting since we indicated the language `html` after the ```.

```html
<div class='awesome' id='more-awesome'>
  <p>This is text in html</p>
</div>
```

The following represents two other examples using JavaScript and CSS syntax highlighting.

```markdown
    ```javascript
        function logTheThings(stuff) {
          console.log(stuff);
        }
    ```

    ```css
        .awesome {
          background-color: #FCCFCC;
        }
    ```
```

Here are some suggested formatting guidelines when writing code blocks:

- JavaScript statements should end with a `;` semicolon
- Comments made should have a space between the comment characters and the comment themselves
    ```javascript
    // Like this
    ```

### Links

Use Markdown style links in your articles to link to other websites.

```markdown
[freeCodeCamp](https://www.freecodecamp.org/)
```

### Images

For including images, if they aren't already hosted somewhere else on the web, you will need to put them online yourself using a platform like [Imgur](https://imgur.com/) or [Flickr](https://www.flickr.com). You can also host images by committing them to a git repository and pushing it to GitHub. Then you can right-click the image and copy its URL.

We don't allow hosting images directly in the git repository because it would make it far too big (people pulling it to their local system to make changes would end up downloading all the images), and because it is easier to change an image by just changing the URL in an article than by putting the new image in the repository.

To include the image in your article, use the appropriate markdown syntax:

```markdown
![Image Title](https://url-to-image)
```

Then the images should show up when you click the <kcd>Preview</kcd> tab.

You can also add diagrams, graphics, or visualizations as necessary.

You can even embed relevant YouTube videos and interactive [REPL.it](https://repl.it/) code editors.

Don't use emojis or emoticons in the Guide. freeCodeCamp has a global community, and the cultural meaning of an emoji or emoticon may be different around the world. Also, emojis can render differently on different systems.

### Attributions

To minimize the potential for plagiarism and maintain integrity in these guides, it is important to give credit where necessary.

Any material quoted, or used directly and unchanged, from source material should be wrapped in quotation marks and be adequately cited. Material that is not a direct quote but is still paraphrased from a different resource should also be cited.

You can create superscript numerals to mark content that is cited using `<sup></sup>` tags.

Like so: <sup>1</sup>

1. freeCodeCamp - Attributions

Then, at the bottom of your article, place a

```markdown
### Sources
```

heading and include all of your citations numbered to correspond with your sources.

An example is highlighted below.

```markdown
Here is some content that should be cited.<sup>1</sup>

And here is even more that should be cited from another source.<sup>2</sup>

### Sources

1. [Doe, John. "Authoring Words." *WikiCoder*. January 1, 1970. Accessed: October 20, 2017](#)
2. [Purdue OWL Staff. "MLA Works Cited: Electronic Sources." *Purdue Online Writing Lab.* October 12, 2017. Accessed: October 20, 2017.](https://owl.english.purdue.edu/owl/resource/747/08/)
```

You can check out the Purdue link above to see how to properly cite web sources (they even show how to cite tweets!).

Typically, an attribution has a structure like the following:

> Author Last Name, Author First Name. "Article Title." *Publication.* Publisher. Date Published. Date Accessed.

If you cannot find an author or published date, which is common, simply omit these.

Use of proper citations will not only keep the guides reputable, but these citations and links will also provide valuable resources should the reader want to learn more about the topic.

Also note that instances of blatant plagiarism will be either removed or have their pull requests declined, and the user will receive a warning.

Please refer to and review freeCodeCamp's [Academic Honesty Policy](https://www.freecodecamp.org/academic-honesty) before contributing.

### Resources

If there are other Guide resources you think campers would benefit from, add them at the bottom in a "Resources" section with a bulleted list.

```markdown
### Resources

- [A New Resource](#link)
```

### Formatting

Use double quotes where applicable.

Format language keywords as code - this is done with the backtick key (located to the left of the "1" key on a US keyboard) in GitHub-flavored markdown. For example, put back ticks around HTML tag names or CSS property names.

Use the Oxford Comma when possible (it is a comma used after the penultimate item in a list of three or more items, before ‘and’ or ‘or’ e.g. an Italian painter, sculptor, and architect). It makes things easier, clearer, and prettier to read.

## Technical Writing

Technical writing, or the literature of science and technology, is hard.

You'll need to take a technical (usually abstract) topic and explain it in a clear, accurate, and objective manner.

You'll likely go through several rounds of proofreading and editing before you're happy with the result.

### Outline

Before you begin writing, create an outline of the topic and think about any coding examples you'll use (if applicable).

This helps to organize your thoughts and make the writing process easier.

### Intro

The introduction paragraph should only be 1-2 sentences long and be a simple explanation of the main topic. It should limit the use of any links to other Guide articles, as they can be distracting.

### Content

Keep paragraphs short (around 1-4 sentences). People are more likely to read several short paragraphs over a wall of text.

### Clarity

Articles should be written with short, clear sentences, and use as little jargon as necessary.

All jargon should be defined immediately in plain English.

### Voice

Use active voice instead of passive voice. Generally, it's a stronger and more straightforward way to communicate a subject. For example:

#### Passive

The `for` loop in JavaScript is used by programmers to...

#### Active

Programmers use the `for` loop in JavaScript to...

### Point of View

Text should use the second person ("you") to help to give it a conversational tone.

This way, the text and instructions seem to speak directly to the camper reading it.

Try to avoid using the first person ("I", "we", "let's", and "us").

### Abbreviations

If you want to abbreviate a term in your article, write it out fully first, then put the abbreviation in parentheses.

For example, `"In computer science, an abstract syntax tree (AST) is ..."`

### Proper nouns

Proper nouns should use correct capitalization when possible. Below is a list of words as they should appear in Guide articles.

- JavaScript (capital letters in "J" and "S" and no abbreviations)
- Node.js

Front-end development (adjective form with a dash) is when you working on the front end (noun form with no dash). The same goes with the back end, full stack, and many other compound terms.

### Third-Party Tools

To check for grammar and spelling, we recommend using an app like [Grammarly](https://grammarly.com) or a built in extension/plugin that checks for this within your text editor.

- [VS Code](https://code.visualstudio.com/) - [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
- [Sublime Text 3](https://www.sublimetext.com/docs/3/spell_checking.html)

To check your writing style, we recommend the  [Hemingway App](http://www.hemingwayapp.com/).

There’s nothing magical about this simple tool, but it will automatically detect widely agreed-upon style issues:

- passive voice
- unnecessary adverbs
- words that have more common equivalents

The Hemingway App will assign a "grade level" for your writing.

You should aim for a grade level of 6.

Another tool available is the [De-Jargonizer](http://scienceandpublic.com/), originally designed for scientific communication but might help avoid overspecialized wording.

---

# Reviewing PRs

> This section is targeted at reviewers of this repo.

## Squash and Merge

We use the <kcd>Squash and merge</kcd> option when merging the PR which keeps the commit history clean.

![GIF - Squash and merge](https://files.gitter.im/FreeCodeCamp/Contributors/56MQ/9cb8db153d7bb1b3576cd1ffc207e39d.gif)

## Filtering PRs

> PR, Open, Oldest First, Travis CI Build successful, no one assigned, no comments

[`is:pr is:open sort:updated-asc status:success no:assignee comments:0`](https://github.com/freeCodeCamp/guides/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Aopen%20sort%3Aupdated-asc%20status%3Asuccess%20no%3Aassignee%20comments%3A0)

> PR, Open, Oldest First, Does not have labels: `platform`, `enhancement`, `invalid` or `changes requested`

[`is:pr is:open sort:updated-asc -label:platform -label:enhancement -label:invalid -label:"changes requested"`](https://github.com/freeCodeCamp/guides/pulls?utf8=%E2%9C%93&q=is%3Apr%20is%3Aopen%20sort%3Aupdated-asc%20-label%3Aplatform%20-label%3Aenhancement%20-label%3Ainvalid%20-label%3A%22changes%20requested%22).

## Templates

> You can make your own with GitHub's built in [**Saved replies**](https://github.com/settings/replies/) feature or use the ones below.

### Build Error

```markdown
Hey @username

So I'd love to be able to merge your changes but it looks like there is an error with the Travis CI build. ⚠️

Once you resolve these issues, I will be able to review your PR and merge it. 😊

---

> Feel free to reference the [Article Style Guide](https://github.com/freeCodeCamp/guides#article-title) for this repo on formatting an article correctly so your Travis CI build passes. ✅
>
> Also, it's good practice on GitHub to write a brief description of your changes when creating a PR. 📝
```

### Syncing Fork

> When PR is not up to date with `master` branch.

``````markdown
Hey @username

So I'd love to be able to merge your changes but it looks like there is an error with the Travis CI build. ⚠️

```bash
Error: ENOTDIR: not a directory, open 'src/pages/java/data-abstraction/index.md'
```

This particular error was not actually caused by your file but was an old error caused by merging faulty code to the `master` branch. It has since been resolved.

To pass the build, you will have to sync the latest changes from the `master` branch of the `freeCodeCamp/guides` repo.

Using the command line, you can do this in three easy steps:

```bash
git remote add upstream git://github.com/freeCodeCamp/guides.git

git fetch upstream

git pull upstream master
```

If you're using a GUI, you can simply `Add a new remote...` and use the link `git://github.com/freeCodeCamp/guides.git` from above.

Once you sync your fork and pass the build, I will be able to review your PR and merge it. 😊

---

> Feel free to reference the [Syncing a Fork](https://help.github.com/articles/syncing-a-fork/) article on GitHub for more insight on how to keep your fork up-to-date with the upstream repository. 🔄
>
> Also, it's good practice on GitHub to write a brief description of your changes when creating a PR. 📝
``````

### Merge Conflicts

> When PR has merge conflicts that need to be resolved.¹

```markdown
Hey @username

So I'd love to be able to merge your changes but it looks like you have some merge conflicts. ⚠️

Once you resolve these conflicts, I will be able to review your PR and merge it. 😊

---

> If you're not familiar with the merge conflict process, feel free to look over GitHub's guide on ["Resolving a merge conflict"](https://help.github.com/articles/resolving-a-merge-conflict-on-github/). 🔍️
>
> Also, it's good practice on GitHub to write a brief description of your changes when creating a PR. 📝
```
¹ If a first-time-contributor has a merge conflict maintainers will resolve the conflict for them.

### Duplicate

> When PR is repetitive or a duplicate.

```markdown
Hey @username

It seems that similar changes have already been accepted earlier for this article you're editing, sorry about that. 😓

If you feel you have more to add, please feel free to open up a new PR.

Thanks again! 😊

---

> If you have any questions, feel free to reach out through [Gitter](https://gitter.im/FreeCodeCamp/Contributors) or by commenting below. 💬
```

### Closing

> When PR is invalid.

```markdown
Hey @username

You haven't actually added any content so I will be closing this PR and marking it as `invalid`. 😓️

Feel free to open another PR though! 👍
```
