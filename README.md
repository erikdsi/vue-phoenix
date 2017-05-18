#Vue2.x boilerplate for Phoenix

> Vue2.x+Webpack2 setup for [Phoenix](http://www.phoenixframework.org/)
> If you want a standalone Vue+Webpack check [Webpack](https://github.com/vuejs-templates/webpack)

## Usage


This is a project template for [vue-cli](https://github.com/vuejs/vue-cli). **It is recommended to use [yarn](https://yarnpkg.com/en/) or npm 3+ for a more efficient dependency tree.**

``` bash
$ mix phoenix.new my-project --no-brunch
$ yarn global add vue-cli
$ vue init erikdsi/vue-phoenix my-project
$ cd my-project
$ yarn install
```
You still have to manually change a line in your `config/dev.exs` to get it to work
``` elixir
watchers: [npm: ["run", "watch"]]
```
And then finally:
``` bash
$ mix phoenix.server
```

## What's Included

- Webpack + `vue-loader` for single file Vue components.
- Babel configured to transpile to js that works in old devices(ios 7)
- SCSS extraction
- Pug for templates(former jade)
- [vue-resource](https://github.com/pagekit/vue-resource) So you can make http requests
- [vue-router](https://github.com/vuejs/vue-router)



