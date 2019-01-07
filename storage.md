# Storage 

## localStorage

localStorage is a built-in storage API for the browser and saves the stored data across browser sessions, meaning it will hold on to the data even if the browser tab is closed.

```
localStorage.setItem('key', 'value'); 
```
However, it's important to note that localStorage can only store strings. If you need to use another datatype, string conversion or another storage method is needed. The way to convert data is using the `JSON.stringify()` method. 

```
const names = ['Violet', 'Klaus', 'Sunny']
window.localStorage.setItem('user', JSON.stringify(names));
```
## Cookies 

Cookies deal with keeping a user logged into a browser's session. Conceptually, a session holds data associated with a particular HTTP client and persists across multiple requests from the same client. Sessions have no inherent understanding of "users", just the idea of persisting data across many different request/response cycles between the same server and client. Cookies are a feature of HTTP that circumvents its statelessness. Each client get its own session store on the server.

Cookies are a small text file with key-value pairs 
```
Set-Cookie: <cookie-name>=<cookie-value>
```
Create

## Comparisions between localStorage, cookies, and indexDB 

Cookies can be maniulated by the web server, unlike localStorage. 
localStorage does not expire, unlike cookies. 