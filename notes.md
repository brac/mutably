# Mutably Exercise

Currently Mutably is no longer an app on heroku. I may be able to use a differnt public api like Random user generator, but I will have to work around not being able practice some of the methods, like PUT and DELETE.

I could make my own RESTful API and deploy that to Heroku (even by the same name?) which would be a lot of good practice.

First I will do the google fetch lab

Now that that's done...

I think that the fastest way will be for me to take the base code that was left on the LG github page and deploy my own copy of mutably. I've removed the branding and now I have a plan. Assume I can get it to deploy things should go like this.

### Plan:
  * Get the app running locally
  - Deploy the app to Heroku
  - Fork scaffolding
  - Plan App




*Notes:*
How do I list all the objects in a mongo db?
```bash
mongo
show dbs
use <db>
show collections
db.collection.find()
```

How do I reset / seed the database?
`POST` to `/reset` or navigate to `/reset` for a button

What is my heroku URL?
`heroku info -s | grep web_url | cut -d= -f2`

## Original Specs
### Description

[Mutably](http://mutably.herokuapp.com/) is a mutable, RESTful, CRUD API. This means that it has endpoints that you can interact with RESTfully via a front-end.

Visit the repo page for information about the resources available and how to interact with them: [https://github.com/GuildCrafts/mutably](https://github.com/GuildCrafts/mutably)

Your goal is to build a front-end that consumes the Mutably API. You can choose any one of the 3 resources. You front-end needs to complete all of the CRUD (Create, Read, Update, Delete) functions.

For the goal, you will start with [this scaffolded template](https://github.com/GuildCrafts/mutably-starter). Fork to get started.
You will use jQuery to complete this goal.

### Context

Interacting with a third-party API is a key skill for any developer. Most APIs have extensive documentation and require a fair amount of "overhead" just to get started working with them.

Not Mutably. This API is _way_ simpler, with just a few _endpoints_ handling a few different _resources_.

This goal is designed as an introduction to working with third-party APIs so that you can familiarize yourself with the core ideas before moving on to work with bigger, more complex APIs (like GitHub or Twitter).

### Specifications

- [ ] __5:__ Your repo is a fork of [mutably-starter](https://github.com/GuildCrafts/mutably-starter).
- [ ] __5:__ Your repo has a README with instructions for how to run your project.
- [ ] __15:__ Your app is SPA (single page app). All CRUD actions take place on the same page, preferably the root (`/`) route.
- [ ] __10:__ All interaction with the API happens with jQuery's AJAX function -- don't submit data via forms. You can use `form` html tags, but do all your form submission in your `js`. Make use of jQuery's `event.preventDefault()`.
- [ ] __15:__ A user can read and display all the data for a resource.
- [ ] __10:__ A user can create a new item via a create form. When the user creates a new item, that item should either get appended to the page or all the items should get re-retrieved in the `js`. No full page refresh.
- [ ] __10:__ A user can update an existing item. Updating happens inline. This means that there is an edit button next to each item that, when clicked, the item text gets replaced with an pre-populated editable, input field. And the edit button becomes a save button. Once the save button is clicked and success message comes back from the server, then then input gets replaced with the updated text. No page refresh.
  For example, this: <br>
  <img width="229" alt="screen shot 2017-05-11 at 3 26 09 pm" src="https://cloud.githubusercontent.com/assets/3010270/25974508/4ac57980-365e-11e7-8b1f-6cf9eefaac22.png">
  <br>
  becomes:
  <br>
  <img width="253" alt="screen shot 2017-05-11 at 3 26 18 pm" src="https://cloud.githubusercontent.com/assets/3010270/25974512/5024433e-365e-11e7-802f-c60afacddecd.png">
  <br>
  When the user clickes the edit button.
- [ ] __10:__ A user can delete an existing item via a delete button next to each item. No page refresh.
- [ ] __10:__ Use a UI library to make your site look nice.
- [ ] __5:__ The artifact produced is properly licensed, preferably with the MIT license.
- [ ] __5:__ App is deployed on Heroku.

#### Stretch

- [ ] Create another version of your front-end using a front-end framework such as React or Angular.

---

***If the mutably data gets too crazy from people adding / deleting things, you can reset the data to the seed data [here](http://mutably.herokuapp.com/).***

***Insider tip: there is an example "solution" (remember, there are MANY ways to hack it!) in the [solution branch](https://github.com/GuildCrafts/mutably-starter/tree/solution) of the starter template.***
