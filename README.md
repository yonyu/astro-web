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

    node --version

    npm create astro@latest

then follow the on-screen instructions.

enter the project folder

code .

Install 'astro' extension as prompted.
also install 'MDX' by unified

Astro has two special folders. Both are under src/:

pages

content


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


