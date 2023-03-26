# Vue + Nuxt Workshop - 18/04/2023 @ Mohole

[ ITA ]
In questa giornata vedremo come realizzare da zero un catalogo dei personaggi della serie "Rick & Morty" utilizzando il framework Nuxt (_basato su Vue.js_) e una fonte di dati pubblica (https://rickandmortyapi.com/).

## Requirements

- [Node.js](https://nodejs.org/) v16+
- [VS Code](https://code.visualstudio.com/)
- [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (_VS Code extension_)
- [Vue developer tools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en) (_browser extension_)
- [Vercel](https://vercel.com/) free account

## What we are using

- [Vue 3](https://vuejs.org/) - reactive UI library
- [Nuxt 3](https://nuxt.com/) - web framework for Vue
- [SASS](https://sass-lang.com/) - CSS with superpowers
- [Bootstrap 5](https://getbootstrap.com/) - CSS UI library

## API

The API consumed by the application is [https://rickandmortyapi.com/](https://rickandmortyapi.com/) , which is a public and free API useful for learning and practice, based on the popular animated series.

## Publish

## Repository structure

| Folder          | Description                          |
| --------------- | ------------------------------------ |
| `(root)`        | main config files                    |
| `/fundamentals` | theory introduction files            |
| `/components`   | components for UI                    |
| `/pages`        | components that will behave as pages |
| `/layouts`      | shared layout elements               |

## Getting started

Clone the repo

```bash
$ git clone https://github.com/mohole/vue-workshop
```

change to project folder

```bash
$ cd vue-workshop
```

install the dependencies

```bash
$ npm ci
```

start the local development server

```bash
$ npm run dev
```

you can now check your application at `http://localhost:3000`.

## Where to go from here

Feel free to enhance and add features to this project since it's just a sample to give you a glimpse on the basics functionalities of Nuxt and Vue:

- design a better UI (_with or without Bootstrap_)
- integrate other APIs from the service, you have also access to `/character` and `/location`
- add filters for easily find content
- enhance the pagination component

or ultimately...

- re-use the code of this project with a **completely different data source** ([https://github.com/public-api-lists/public-api-lists](https://github.com/public-api-lists/public-api-lists))

## License

Released under the [MIT License](LICENSE).
