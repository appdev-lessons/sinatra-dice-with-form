# Sinatra: Dice with Form

In this project, we'll use what we've learned about [query strings and forms](https://learn.firstdraft.com/lessons/102-query-strings-and-forms) to build a version of our dice roll app that allows users to type into forms. At last!

Here is our target:

[dice-form.matchthetarget.com](https://dice-form.matchthetarget.com/)

## Create a codespace

We'll use the `appdev-projects/sinatra-dice-form` repository for this project. 

This project includes automated tests, so click on this button to get started:

LTI{Load Sinatra Dice Form assignment}(https://grades.firstdraft.com/launch)[S9ymPy6WCsn18gLbByVbZQ7k]{vfdtzJb5bLYqYwuqgeRKpc5d}(10)[Sinatra Dice Form Project]

Then, fork the repository and create your codespace.

## /process_roll action

First, let's implement a URL `/process_roll` which, if there's a query string on the end with the keys `dice` and `sides`, will display a page with the appropriate number of random rolls.

For example, if the user visits:

```
/process_roll?dice=5&sides=4
```

Our app should display [a page like this](https://dice-form.matchthetarget.com/process_roll?dice=5&sides=4). The page should work for any two numbers, provided that the keys are exactly `dice` and  `sides`.

## Make it easier for users

Now that `/process_roll` works, assuming that users type an appropriately structured query string into the address bar, let's make it easier for them.

Add a form to the homepage that will send users to `/process_roll` when submitted. The form should also assemble a query string with the keys `dice` and `sides`, with the values entered into the respective fields by the user.

## Forms are two actions working in tandem

Notice that each of the two actions are completely independent — a user can visit only one, and the other may never be visited at all. But the two actions work in tandem to make it easy for non-developer users to interact with our app.

It's tempting to think that a form is just one action, but resist! One action _displays the form_, and the other action _processes the inputs_.

---
