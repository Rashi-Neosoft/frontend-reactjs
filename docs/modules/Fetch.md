
## [**Fetch**](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

Next.js has a built-in polyfill for the fetch API. You don't need to worry about using it on either server or client side.


The Fetch API provides an interface for fetching resources (including across the network). It will seem familiar to anyone who has used XMLHttpRequest, but the new API provides a more powerful and flexible feature set.

The fetch method only has just one compulsory argument, there are other arguments, but the compulsory one is the URL of the resource you wish to fetch. It may be the URL of a website which you want to make the request from. This shouldn’t be difficult because these URLs or links are already provided in the websites or places we are trying to make requests from.
an example of such URL is openweathermap’s API URL
https://api.openweathermap.org/data/2.5/weather?q=lagos&appid={api key}


A basic way to make a fetch request using this URL is to do something like this:

```
fetch(
https://api.openweathermap.org/data/2.5/weather?q=lagos&appid={api key}
)
.then(response => response.json( ))
.then(json => console.log(response.json( ))
```

Another way to make this same request is by using async/await syntax. This syntax was introduced in ES2017 and is quite nice to use. Marking a function as async means that we can wait for its response using the await syntax, and when we get the response, we can then use it as we want.

```
const weather = async () => {
const response = await fetch( https://api.openweathermap.org/data/2.5/weather?q=$lagos&units=metric&appid=${api.key}`
)
const myJson = await response.json();
} 

weather();
```

[View Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)