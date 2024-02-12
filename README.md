# Bold Docs

Bold Theme Documentation powered by [VitePress](https://vitepress.dev/).

## Prerequisites

- [Node.js](https://nodejs.org/) version 18 or higher.
- Terminal for accessing VitePress via its command line interface (CLI).
- Text Editor with [Markdown](https://en.wikipedia.org/wiki/Markdown) syntax support.
    - [VSCode](https://code.visualstudio.com/) is recommended, along with the [official Vue extension](https://marketplace.visualstudio.com/items?itemName=Vue.volar).

## Setup

Install dependencies by running:


```bash
npm install
```

## Up and Running

The following npm scripts are available:

```json
{
  "scripts": {
    "docs:dev": "vitepress dev",
    "docs:build": "vitepress build",
    "docs:preview": "vitepress preview"
  },
}
```

### Development

The `docs:dev` script will start a local dev server with instant hot updates. Run it with the following command:

```bash
npm run docs:dev
```

The dev server should be running at `http://localhost:5173`. Visit the URL in your browser to see your new site in action!

### Build and Test Locally

1. Run this command to build the docs:

```bash
npm run docs:build
```

2. Once built, preview it locally by running:

```bash
npm run docs:preview
```

The preview command will boot up a local static web server that will serve the output directory `.vitepress/dist` at `http://localhost:4173`. You can use this to make sure everything looks good before pushing to production.
