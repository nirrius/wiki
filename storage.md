# Storage 

## localStorage

localStorage is a built-in storage API for the browser and saves the stored data across browser sessions, meaning it will hold on to the data even if the browser tab is closed.

```js
localStorage.setItem('key', 'value'); 
```
However, it's important to note that localStorage can only store strings. If you need to use another datatype, string conversion or another storage method is needed. The way to convert data is using the `JSON.stringify()` method. 

```js
const names = ['Lorem', 'Ipsum', 'Dolo']
window.localStorage.setItem('user', JSON.stringify(names));
```
## Cookies 

Cookies deal with keeping a user logged into a browser's session. Conceptually, a session holds data associated with a particular HTTP client and persists across multiple requests from the same client. Sessions have no inherent understanding of "users", just the idea of persisting data across many different request/response cycles between the same server and client. Cookies are a feature of HTTP that circumvents its statelessness. Each client get its own session store on the server.

Cookies are a small text file with key-value pairs that can be as simple as describing the session id.
```
Set-Cookie: <cookie-name>=<cookie-value>
```
Cookies are created by a server handling a HTTP request and then passed onto the browser for safe keeping. 

So in summary, servers create and browsers store. This system enables information to persist across requests throughout a particular client and server relationship. When that client makes any future requests, the cookie will come along with it. 

## IndexedDB

IndexedDB, also known as the Indexed Database API, is a NoSQL storage system for storing data in JSON object form organized by indices. This enables object retrival with a specific index. 


WebSQL

## Comparisions between localStorage, cookies, and indexDB 

Cookies can be manipulated by the web server, unlike localStorage. 
localStorage does not expire, unlike cookies. 