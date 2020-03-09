# Visual Assets for lib-js

This document is a sub-part of https://github.com/pryv/assets-pryv.me documentation.

It describes the external assets used by https://github.com/pryv/lib-js 

## Content of `lib-js`properties for assets

```json
{ 
  "lib-js": {
    "buttonSignIn": {
      "css": "lib-js/buttonSignIn.css",
      "html": "lib-js/buttonSignIn.html",
      "messages": "lib-js/buttonSignInMessages.json"
    }
	}
}
```

### ButtonSignIn

#### Definitions

- **html** The HTML code representing the Button
- **css** The CSS code related to the Button
- **messages** To customize the different messages depending on the state of the Auth Process
  - LOADING: During the loading of the button (Usually not visible as the loading takes care in less that 150ms)
  - ERROR: Display on Error
  - LOGIN: Text displayed on the button when a Login or Sign-in is required
  - LOGOUT_CONFIRM: Text displayed in an alert message box to confirm Log-out or Sign-out

#### Files

- **buttonSignIn.css** CSS content (declared by property css)
- **buttonSignIn.html** HTML content (declared by property html)
- **buttonSignIn.png** Image for the button for non CSS3 compatible browsers
- **buttonSignInLogoOnly.png** Image for the button for CSS3 compatible browsers
- **buttonSignInMessages.json** Messages definitions (declared by property messages)