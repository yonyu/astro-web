# Astro Starter Kit: Minimal

```sh
npm create astro@latest -- --template minimal
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/minimal)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/minimal)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/minimal/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).


# Create an Astro project

Check node version

    node --version

Create a new Astro project

    npm create astro@latest

then follow the on-screen instructions.

Enter the project folder
    cd project-folder

Launch the node at the project folder
    code .

Install 'astro' extension as prompted.
Also install 'MDX' extension by unified

Astro has two special folders. Both are under src/:
- pages
- content

pages/ folder

there is a file index.astro. astro use it for page routes.

telemetry

[Astro team collects development info](https://astro.build/telemetry/)

run the following command to disable telemetry collection:

    npx astro telemetry disable


# Astro Basics

## Rendering modes

- By default, Astro applies 'Static site generation' (SSG)
  - output: 'static' // fully static, in dist/ folder
- Server-side rendering (SSR)
  - output: 'server' // mostly SSR, some static
  - output: 'hybrid' // mostly static, some SSR

## Components

Any file with '.astro' extension is an Astro component. It can have two sections.

Script section

template section

### Styling

Using style tag
- Will create a data scope
  
Template directives
- `is:global`

Using script tag
- script inside script tag will be sent to the client side

    npm run build

    npm run preview

- script attributes
  
  - async = is:inline async
  - is:inline
  - is:global
- script src attribute
  - can reference external scripts
  
### Astro props

Astro.props is astro global object that is only available on .astro files


## Routing

Astro uses file-based routing. Each file in the pages/ directory is a route.

### about.astro

### contact.md

### html pages are supported

### dynamic routes

Create articles folder under pages folder, then create a page [title].astro

`src/pages/articles/[title].astro`

    npm run dev

In the browser, navigate to: http://localhost:4321/articles/learning-javascript

Rename the file to [id]-[title].astro

`src/pages/articles/[id]-[title].astro`

In the browser, navigate to: http://localhost:4321/articles/1-learning-javascript

### routing markdown files

Create a folder 'posts' under 'pages' folder

Create a markdown file '1-post.md' under 'posts' folder

Can access the file at: http://localhost:4321/posts/1-post

Use index.astro to list all martdown posts

    const posts = await Astro.glob('./*.md')

it has `frontmatter` property:
    
        const { title } = posts[0].frontmatter.title

## Islands architecture of Astro

### What is hydration?

Hydration is the process of turning static HTML into a fully interactive web page.

Hydration is when we add client-side JavaScript to a web page that has already been rendered statically or with
server-side rendering. Hydration makes the web page interactive and dynamic. 

Hydration can be simply as adding an event listener to a static HTML button that has been rendered on the page.

#### Selective hydration

Astro islands architecture involves *selective hydration*.

Selective hydration is the process of choosing which parts of the page to hydrate and which parts to leave as static HTML.

Astro uses islands architecture to selectively hydrate parts of the page.

### What is islands architecture?

Astro uses islands architecture to hydrate only the parts of the page that need to be interactive.

Islands architecture is defined as an architecture where a web page content is generated at build time or demand by 
a web server and then certain sections of the web page are selectively hydrated by the client-side JavaScript.

The islands architecture results in much faster rendering performance as page content is ready to render, and
client side JavaScript is only used selectively.

Script tags can be used inside Astro components. It is a form of hydration. But it is important to note that
the scripts inside Astro components run in the global scope, so they are not considered to be islands.

We can use components from different frameworks or libraries in the same Astro page. This is possible because
Astro treats each component from different frameworks as island component.

Islands architecture is a great way to implement micro frontends.

### Examples of islands components

Here is a good [example](https://github.com/withastro/astro/tree/main/examples/framework-multiple) of Microfrontends 
with Astro.

## Enable react or vue in Astro

Add react and vue into Astro project

    npx astro add react vue

There are many integrations that are available in Astro project. Check the [list](https://docs.astro.build/en/guides/integrations-guide/)

By default, islands component from other libraries are not hydrated. To hydrate them, use the `client:load` attribute.

    <ReactCounter client:load>


## Advanced Astro

Create a blank Astro project

    npm create astro@latest

Create styles folder under src folder and create a file global.css in it.

Create a layouts folder under src folder and create a file BaseLayout.astro in it.

Create a components folder under src folder and create a file VerticalMenu.astro in it.