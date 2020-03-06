# Visual Assets centralization for Pryv.io 

This repository contains visual assets for the Pryv.me platform. 

The file 'index.json' is exposed to various applications and libraries by `/service/info` API call with the `assets.definitions` property.

This structure is a proposal that can and should be extended depending on the needs of each Pryv.io deployment. 

# Deployement

For Pryv Lab (pryv.me) we deploy the assests using github gh-pages.

## Default structure 

### index.json

- `baseUrl` should be used to resolve  ressource path if not starting with `http(s)://`. If `undefined` or set to `null`, baseUrl should be related to the path of index.json location. 
- `favicon`should have at least `default`property exposing a `.ico` file.
- `css` should have at least `default`property exposing a `.css` file.
- `{app-name}`exposes customs assets per application.

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
    "login-button": {
      "css": "lib-javascript-button.css"
    }
  }
}
```