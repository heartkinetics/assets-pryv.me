# Visual Assets centralization for Pryv.io 

This repository contains visual assets for the Pryv.me platform. 

The file 'index.json' is exposed to various applications and libraries by `/service/info` API call with the `assets.definitions` property.

This structure is a proposal that can and should be extended depending on the needs of each Pryv.io deployment. 

# Deployement

For Pryv Lab (pryv.me) we deploy the assests using github gh-pages.

The file `index.json` is declared in the `service-info`configuration part of global **Pryv.io**'s' settings. 

Example: https://reg.pryv.me/service/infos

```json
{
  "access": "https://access.pryv.me/access",
  "api": "https://{username}.pryv.me/",
  "serial": "2019061301",
  "register": "https://reg.pryv.me",
  "name": "Pryv Lab",
  "home": "https://sw.pryv.me",
  "support": "https://pryv.com/helpdesk",
  "terms": "https://pryv.com/terms-of-use/",
  "event-types": "https://api.pryv.com/event-types/flat.json",
  "assets": {
  	"definitions": "https://pryv.github.io/assets-pryv.me/index.json"
	}
}
```



## Default structure 

### index.json

- `baseUrl` should be used to resolve  ressource path if not starting with `http(s)://`. If `undefined` or set to `null`, baseUrl should be related to the path of index.json location. 

- `favicon`should have at least `default`property exposing a `.ico` file.

- `css` should have at least `default`property exposing a `.css` file.

- `{app-name}`exposes customs assets per application.

  ​	See: https://github.com/pryv/assets-pryv.me/tree/master/lib-js as example of App specific definitions

```json
{ 
  "baseUrl": null,
  "favicon": {
    "default": "favicon.ico"
  },
  "css": {
    "default": "default.css"
  },
  "lib-js": {
    "buttonSignIn": {
      "css": "lib-js/buttonSignIn.css",
      "html": "lib-js/buttonSignIn.html",
      "messages": "lib-js/buttonSignInMessages.json"
    }
  }
}
```