# ALLWEB Vue Presentation
### 28 March 2019, By Chungphing LY

[Link to Slides](https://docs.google.com/presentation/d/1kKsoH7Zs0MhGzMernuXLddNZwiiQMOMaq-i5DKBak90/edit?usp=sharing)
___

# Setting up environment

## Installing Node.JS and NPM

* Go to nodejs.org and download the lts version of Node.js
* After installing Node, make sure you can access node and npm by using `node -v` and `npm -v`

## Installing Vue CLI

In this tutorial, we'll use Vue CLI to scaffold our project. Please noted that, Vue CLI is not designed for beginner. But since our team already have some experience with web development, I think this is fine considering our time constraint.

In the terminal, Use this command  

`npm install -g @vue/cli`

After installation, check if vue is install correctly using

`vue --version`

If you see `3.x.x`, then you have install Vue CLI correctly.

## Creating Our Project

Now we can use Vue CLI to scaffold our project

In the terminal, `cd` to your desired folder. and use  

`vue create vue-todo`

For configuration please choose default option:

After it generates our project use

`cd vue-todo` and `npm run serve` to fire up a dev server. now we can start building our application.
___
# Developing
## Create Components

For a Todo app, we'll need  
* List of Todos `Todos`
    * Individual Todo item `TodoItem`
        * A Checkbox
        * An Input Field
        * A Delete Button
* Form input to add new Todo `AddTodo.vue`
    * Input Field
    * A Button

This will give us an idea how a complex application is developed

### TodoItem

Let's us start from the smallest component.

