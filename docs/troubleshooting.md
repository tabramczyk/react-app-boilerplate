# Troubleshooting 

## Rendering doesn't work correctly

This app uses SSR streaming that is not supported by jss library (material-ui uses jss).

To fix this problem you need to edit [src/server/index.js](../src/server/index.js)

Follow the steps below:

* remove streaming  
* add JssProvider (and MuiThemeProvider if you use material-ui)
* prepare html template and send it to the client

If you need help:

* [ReactDOMServer](https://reactjs.org/docs/react-dom-server.html)
* [Server Rendering - Material-UI](https://material-ui.com/guides/server-rendering/)
* [Server Side Rendering - styled-components](https://www.styled-components.com/docs/advanced#server-side-rendering)
