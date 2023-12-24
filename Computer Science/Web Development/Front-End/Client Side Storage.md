### Comparison

|              | **Cookies**                                                                              | **Session Storage**              | **Local Strorage**                                                              |
| ------------ | ---------------------------------------------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------------------- |
| **Scope**    | specific to a domain and path, shared across all tabs and windows opened for that domain | specific to a particular tab     | specific to a domain, shared across all tabs and windows opened for that domain |
| **Lifetime** | persist across sessions and can have expiration dates                                    | persists until the tab is closed | persists across sessions                                                        |
| **Storage**  | smallest                                                                                 | middle                           | largest                                                                         | 

### API Methods

##### Cookies
```javascript
// Setting
document.cookie = "username=john_doe; expires=Wed, 31 Dec 2099 23:59:59 GMT; path=/";

// Retrieving
const username = document.cookie.split(';').find(cookie => cookie.trim().startsWith('username='));

// Removing
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/";
```

##### Session Storage
```javascript
// Storing
sessionStorage.setItem('username', 'john_doe');

// Retrieving
const username = sessionStorage.getItem('username');
console.log(username); // Output: john_doe

// Removing
sessionStorage.removeItem('username');

// Clearing
sessionStorage.clear();
```

##### Local Storage
```javascript
// Setting
localStorage.setItem('theme', 'dark');

// Retrieving
const theme = localStorage.getItem('theme');

// Removing
localStorage.removeItem('theme');

// Clearing
localStorage.clear();
```
