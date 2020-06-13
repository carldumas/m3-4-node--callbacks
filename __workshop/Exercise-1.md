# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here

get /
  render the html
  should have a form
  .get('/', (req, res) => {
    load homepage
  })
  .post('/form-data', (req, res) => {
    grab input data
    add it to server data
    reload homepage
  })

```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here

Body Parser parses the input data and converts it in a form that's easier to work with. 
It grabs the ToDoList input and inserts it in a string in the server data.
The line 26 also uses the package
  .use(bodyParser.json())

```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here

GET - get is used to request data from a server and renders the specified page with the new data.
POST - post is used the send data to a server and, in our case, update the variable ITEMS

```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here

It's calling the javascript document HANLDERS and the constant/functions that it contains. The information is in between curly brackets so that our code is DRY.

```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here

It's the array we use to store every input from the to do list

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here

We dont want the user to stay in the url '/form-data', so we redirect him to the main page '/'
We want to refresh the page with the new data in ITEMS

```  

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here

The extra functionality is there to handle the specified media type. 
It returns different errors depending on the type of file received.
when it call the handler 404 if it allow json then it will send a response to that header in a json format.
when it call the handler 404 if it doesn't allow json then it will send back a response to that header in a txt format.

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```

// Answer here

homepage.ejs
  - render the header template from folder partials
  - render the input field template on the homepage
  - loop through all items on server 
  - create list element for each item
  - render the footer template
toDoInput.ejs
  - create a form with a POST request and we send the form to /form-data
  - create label / input / and button to make everything work

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here

```







