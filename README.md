# Vue2.x boilerplate for Phoenix 1.3-rc

> Vue2.x+Webpack2 setup for [Phoenix](http://www.phoenixframework.org/)
> If you want a standalone Vue+Webpack check [Webpack](https://github.com/vuejs-templates/webpack)

## Usage


This is a project template for [vue-cli](https://github.com/vuejs/vue-cli). **It is recommended to use [yarn](https://yarnpkg.com/en/) or npm 3+ for a more efficient dependency tree.**

``` bash
$ mix phoenix.new my-project --no-brunch
$ yarn global add vue-cli
$ vue init erikdsi/vue-phoenix my-project
$ cd my-project/assets
$ yarn install
```
Add the watcher command in your `config/dev.exs`
``` elixir
watchers: [npm: ["run", "watch", "--prefix", "assets"]]
```

Setup your `app.html.eex` and/or `index.html.eex`:

``` html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="<%= static_path(@conn, "/css/app.css") %>">
  </head>
  <body>
    <div id="app"></div>
    <script src="<%= static_path(@conn, "/js/app.js") %>"></script>
  </body>
</html>
```

Setup your PageController

``` elixir
def index(conn, _params) do
  render conn, "app.html"
end
```

And then finally:
``` bash
$ mix ecto.create
$ mix phoenix.server
```

## What's Included

- Webpack + `vue-loader` for single file Vue components.
- Babel configured to transpile to js that works in old devices(ios 7)
- SCSS extraction
- Pug for templates(former jade)
- [vue-resource](https://github.com/pagekit/vue-resource) So you can make http requests
- [vue-router](https://github.com/vuejs/vue-router)

## Useful links

- [Webpack Docs](https://webpack.js.org/configuration/)
- [Vue](https://vuejs.org/v2/guide/)
- [Phoenix](http://www.phoenixframework.org/docs/overview)