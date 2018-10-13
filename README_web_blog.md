# WEB:

 - URL: http://2018.jsday.es/
 - Repo: https://github.com/jsDayES/web2018

La web se despliega de forma manual en gh-pages.

## El entorno

1. Clonar el repo
2. Instalar node (v 8.3) si no lo tienes. Si usas NVM:
   ```
   nvm install
   nvm use
   ```
3. Instalar gulp y dependencias
   ```
   npm install -g gulp
   npm install
   ```

## Comandos básicos

- `npm start` -> Arranca la web en http://localhost:5000 (dev mode)
- `npm run pro` -> Compila la web para producción en `./dist`
- `npm eun server -> Arranca un servidor para testear el código compilado en './dist'
- `npm run deploy` -> Realiza el despliegue a producción. Pushea el contenido de `./dist` a la rama gh-pages.
- `npm run deploy-force` -> Lo mismo que el anterior pero forzando la reescritura del histórico ante cualquier conflicto.

## Desplegar en pro:
```
npm run pro
npm run deploy
```

NOTA: El fichero `CNAME` es importante ya que define la url donde se aloja la web. Debe estar en el directorio dist

## Estructura del repo:

`css/` -> CSS del repo,
`js/` -> Código javascript
`lang/` -> Traducciones para las versiones en español e inglés.
`templates/` -> html de la página principal del repo
`config.json` -> Configuración, úti para activar y desactivar secciones de la web


=====================================
=====================================

# BLOG:

 - URL: https://blog.jsday.es/
 - Repo: https://github.com/jsDayES/blog
 - CI: https://travis-ci.org/jsDayES/blog

El blog se despliega de forma automática en gh-pages desde la rama master gracias a TravisCI.

El blog está desarrollado utilizando Hexo (https://hexo.io/), un generador de web estáticas para blogs escrito en javascript.

## El entorno

1. Clonar el repo
2. Instalar node (v 8.3) si no lo tienes. Si usas NVM:
   ```
   nvm install
   nvm use
   ```
3. Instalar gulp y dependencias

   ```
   npm install -g hexo
   npm install
   ```

## Commands

- `hexo clean` Remove generated files and cache.
- `hexo deploy` Deploy your website.
- `hexo generate` Generate static files.
- `hexo help` Get help on a command.
- `hexo list` List the information of the site
- `hexo new` Create a new post.
- `hexo publish` Moves a draft post from _drafts to _posts folder.
- `hexo server` Start the server.

Mas info en https://hexo.io/docs/commands

## Deploy (to gh pages)

Este es el deploy manual, no es necesario hacerlo ya que cualquier commit a master des desplegará mediante TravisCI automáticamente

```
hexo clean && hexo generate && hexo deploy
```

## El Post

Para escribir post no hace falta descargar el repo, bastará con crear un fichero `.md` en `source/__post/`
(https://github.com/jsDayES/blog/tree/master/source/_posts) con la estructura

```
<año>-<mes>-<dia>-<titulo-del-post>.md
```

Este fichero contien una primera parte Front-matter (https://hexo.io/docs/front-matter) con los metadatos del post y luego el
contenido escrito en Markdown. Si usamos el comando de hexo para general el post se creará un esqueleto con esta estructura si
lo hacemos desde github tendremos que escribirlo nosotros (al menos título y fecha).

Para los assets se pueden seguir estas indicaciones https://hexo.io/docs/asset-folders referentes a post asset.

Hay mucha más info en la documentación: https://hexo.io/docs/
