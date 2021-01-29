# To-do List Project
## Introduction
In this coding tutorial, you will be creating [this](https://youtu.be/hSojFVFGOcw) web application. Throughout the tutprial you will be learn how to:

* Use the command line
* Create and manipulate directories and files through the Terminal
* Commit and push changes to GitHub from the command line
* Write HTML/CSS/JavaScript
* Add the project to CircleCI, and add to the CircleCI config file
* Create an environment variable
* Push your application to Netlify
* Create tests with Cypress
* Store test recordings as artifacts in CircleCI

The goal of this project is to help you understand how web applications are created while using CircleCI for CI and Continuous Deployment. This project is  simple compared to what teams of developers will work on, but it should still give you some insight on how to create a web application while integrating with other tools.

You will see **Learning notes** within the instructions. These notes are not tasks for you to do. They are available for learning purposes and to supplement concepts within the tutorial

I let you know when it's time to push to GitHub. When you see ```git commit -m "create a description here"``` make sure to add a description between the quotation marks. The description should describe the changes you have just made.
 
Let's begin! 

<h2> Clone the project </h2>

**TASK**: Go to [this](https://github.com/radhigulati/todolistactivity) repository, to clone the project. 

**TASK**: To clone the project, go to the green ```code``` button on the repo page, and copy the url for SSH.

**TASK**: Open up your terminal, and check which directory you are in with the command ```pwd```.

**TASK**: You should be in the ```projects``` directory. If you aren't, and you are in your home directory (```/Users/radhika```) then type in the command ```ls``` to see the list of directories you can access.

**TASK**: You should see the ```projects``` directory, and you can use the command ```cd projects``` to access this directory.

Type the command ```git clone git@github.com:radhigulati/todolistactivity.git```.

**TASK**: Once you've cloned the project, you should see it in your projects folder. Type the command ```ls``` to list your files. 

<h2> Add project to GitHub </h2>
Let's create the GitHub repo before we get started.

To add the project to GitHub, follow the instructions below:

<h2>Add project to GitHub</h2>

<span style="color:red"> **TASK:** </span>Let's navigate to GitHub and create a new project. Within GitHub, navigate to the ```new``` button to create a new project. For the ```repository name``` use ```todolist```. You can add a description that says ```This project is a beginner git project.``` Make the project ```public```. Then click ```create repository```.

You have now created an empty repository within GitHub.

<span style="color:red"> **TASK:** </span> Now, we need to point our local repository to the remote repository. To do that type the following command in your terminal (make sure you are in your project directory)
```git remote add origin [repository url]```

The ```repository url``` will be ```git@github.com:[your github username]/[name of repo].git```. For example, my url would be ```git@github.com:radhigulati/todolist.git```

<span style="color:red"> **TASK:** </span> Let's push your project to GitHub. To do this, type the command ```git push -u origin main``` or ```git push -u origin master```
if the branch name is still master.

If you navigate to GitHub, you should see your file in GitHub!

---

Type the command ```cd todolist``` to access the project. 

Now you are in the project directory. Let's open this project within our text editor. Remember, with VScode, you can type the command ```code .``` within your Terminal and open the project from there.

Once you've opened the project, let's take a look at what it looks like on a web page. If you are using VScode, right click in the html file and choose ```open in live server```. When you do this, the file will open up in your browser, and you should see see a web page. You'll notice the web page is not complete, but we'll fix that! 

If you go back to the text editor, you'll see a list of files. Let's go through these files and take a look at each one.

Let's first take a look at the ```index.html``` file. This is the html file for the project.

> **Learning Note:** Learning HTML (HyperText Markup Language) is the standard markup language for creating Web pages. Markup languages are languages used by a computer to annotate a document. Markup languages define the style and structure of a document so that a computer knows how you want that document to appear.

An HTML element is defined by a start tag, some content, and an end tag. If we look at the HTML file in our text editor, we see this in action. 

> **Learning Note:** The first line in the file are ```<!DOCTYPE html> <html lang="en">```. A doctype or document type declaration is an instruction which tells the web browser about the markup language in which the current page is written. The Doctype is not an element or tag, it lets the browser know about the version of or standard of HTML or any other markup language that is being used in the document. In the case of our file, we are using HTML 5.

> **Learning Note:** The ```lang``` attribute specifies the language of the element's content. Common examples are "en" for English, "es" for Spanish, "fr" for French and so on.

> **Learning Note:** The ```charset``` attribute specifies the character encoding for the HTML document.

> **Learning Note:** The HTML5 specification encourages web developers to use the UTF-8 character set, which covers almost all of the characters and symbols in the world!

> **Learning Note:** The ```rel``` attribute specifies the relationship between the current document and the linked document/resource.

> **Learning Note:** The ```href``` attribute specifies the URL of the page the link goes to.

The ```<head>``` element is a container for metadata (data about data) and is placed between the ```<html>``` tag and the ```<body>``` tag.

> **Learning Note:** Metadata is data about the HTML document. Metadata is not displayed.
It typically defines the document title, character set, styles, scripts, and other meta information.

The ```<title>``` tag defines the title of the document. The title must be text-only, and it is shown in the browser's title bar or in the page's tab.

The ```<body>``` tag defines the document's body.

The ```<body>``` element contains all the contents of an HTML document, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

Within the ```<body>``` tags in this html file, we have other tags that make up our web page.

<h2> Create a header tag</h2>

The first assignment you need to do is create an ```<h1></h1>``` tag under the header tag in the html document. Within the ```<h1></h1>``` tag you will create the name of your project. This project is a Todo list, so you should name it "My Todo List." [Here](https://www.w3schools.com/tags/tag_hn.asp) is an example of how to use the ```h1``` tag.

Once you've added your ```h1``` tag, open up this file in the live server again, and you should see the header on the web page.

> **Learning Note:** 127.0.0.1 is the loopback Internet protocol (IP) address also referred to as the localhost. The address is used to establish an IP connection to the same machine or computer being used by the end-user. When making network requests, you use an IP address, or a host name, and a port. For example we might have a web server running on our machine. A second web server can be started on a different port.

The next tag we'll look at in the html file is the ```<form>``` tag. 

> **Learning Note:** The ```<form>``` tag is used to create an HTML form for user input.

<h2> Create an input tag </h2>

The ```input``` tag is used to specify an input field where the user can enter data. We need to create an HTML element for the input. To do this you are going to use the ```<input>``` tag. The ```type``` for this ```input``` tag is ```text```. Then you will also add a class of ```"todo-input"```. Check out [this](https://www.w3schools.com/w3css/w3css_input.asp) example to get an idea of how to use the input tag.

Now check out the web page in your browser. You should see the input form now! If you try and type something in it, the text won't get processed just yet. The rest of the HTML file is filled out for you. 

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

Underneath the input, we see a button. The button is right next to the input form on the webpage. 

> **Learning Note:** The class attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.

> **Learning Note:** The button tag has a type of submit. The type attribute specifies the type of button.

Within the button tag, there is a ```span``` tag.

> **Learning Note:** The HTML ```<span>``` tag is used for grouping and applying styles to inline elements.

The ```span``` tag is being used to display an icon. The icons are coming from the [font awesome](https://fontawesome.com/) website. We are importing the icons in the HTML file at the top of the file.

Once we close out the ```form``` tag, we create a ```div```.

> **Learning Note:** The ```<div>``` tag defines a division or a section in an HTML document. It is used as a container for HTML elements - which is then styled with CSS or manipulated with JavaScript. The ```<div>``` tag is easily styled by using the class or id attribute.

With the ```div``` tag in our html file, we created a ```div``` for the todos that will list out once they are added on the webpage. We can style this container or section on our html page through CSS.

Right before we close out the html page, we add a ```script``` tag to link to our JavaScript file. Before we dive into the JavaScript, let's look at our CSS file first.

<h2> CSS File </h2>

Open the CSS file ```style.css```. 

> **Learning Note:** Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS describes how elements should be rendered on screen, on paper, in speech, or on other media. CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

> **Learning Note:** HTML was never intended to contain tags for formatting a web page. HTML was created to describe the content of a web page. When tags like ```<font>```, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process. To solve this problem, the World Wide Web Consortium (W3C) created CSS. CSS removed the style formatting from the HTML page.

A CSS rule-set consists of a selector and a declaration block. The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons. Each declaration includes a CSS property name and a value, separated by a colon.

The first CSS block begins with the ```body``` selector. By selecting the ```body``` you are selecting the entirety of the html document and assigning CSS to the entire document.

As we go down the CSS file, we have more selectors and we are applying styles to these selectors. 

Let's make a couple of changes to this file.

<h2> Adding a background color </h3>

Add a ```background-color``` element in the body selector. You can use [this](https://htmlcolorcodes.com/) color picker to find a HEX value for the ```background-color```. **Don't forget the ```#``` before the hex value.**  

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

<h2> Adding color to the form button </h2>
On the web page, you will notice a button with a square. This is the button that will submit a todo item and a list will be created. Let's add some color to this button. 

Under the form button selector add the ```color``` attribute, and add a hex value like (```#E29178```) as the value. It should look something like:

     color:  #E29178; 
When you refresh the page, you'll see that the button has color. The color changes as you hover over the button because of the ```form button:hover``` selector. The ```:hover``` selector is used to select elements when you mouse over them.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

We'll come back to the CSS once we've added some JavaScript.

<h2> JavaScript </h2>
JavaScript is a text-based programming language used both on the client-side and server-side that allows you to make web pages interactive. Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user. Common examples of JavaScript that you might use every day include the search box on Amazon, a news recap video embedded on The New York Times, or refreshing your Twitter feed.  

>**Learning Note:** The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page. A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

For this project, we are using vanilla JavaScript. 

> **Learning Note** You can use different frameworks like ReactJS, VueJS, etc for different frontend JS frameworks or a framework like Node for backend programming. Both Node.js and React.js are JavaScript frameworks but they are entirely different concepts. The most significant difference between Node.js and React.js is React is used to create user applications, while Node.js is a back-end system. 

Let's take a look at the ```app.js``` file.

We start off by creating variables with ```const``` and setting them equal to specific elements. 

> **Learning Note:** The method querySelector() returns the first Element within the document that matches the specified selector, or group of selectors.

> **Learning Note:** Variables defined with ```const``` behave like ```let``` variables, except they cannot be reassigned.

<h2> Creating a querySelector </h2>

```const todoInput``` and ```const todoButton``` are set to the form input and button elements.

We need to create a const variable for the ```todo-list``` as well. 

**TASK:** Create another querySelector for the ```todo-list``` element. The const variable should be ```todoList```, and the selector passed to the querySelector method should be ```'.todo-list'```. This line should look exactly the same as lines 3 and 4 minus the const name change and selector name change.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

The next section of the JavaScript is for the event listeners. The ```addEventListener()``` method attaches an event handler to the specified element.

<h2> Creating an eventListener </h2>

> **Learning Note:** Events are actions that happen when the user or browser manipulates a page. They play an important role as they can cause elements of a web page to change dynamically. For example, when the browser finishes loading a document, then a load event occurred. If a user clicks a button on a page, then a click event has happened. Many events can happen once, multiple times, or never. You also may not know when an event will happen, especially if it is user generated. In these scenarios, you need an event handler to detect when an event happens. This way, you can set up code to react to events as they happen on the fly. JavaScript provides an event handler in the form of the addEventListener() method. This handler can be attached to a specific HTML element you wish to monitor events for, and the element can have more than one handler attached.

In our case, we need event listeners to **add a todo**, and to **remove a todo**.  

I've already added an addEventListener for adding a todo. We need one for removing an item. 

The syntax for the eventlistener method is 

```target.addEventListener(event, function, useCapture)```

> **Learning Note:** target: the HTML element you wish to add your event handler to. This element exists as part of the Document Object Model (DOM) and you may wish to learn about how to select a DOM element.

> **Learning Note:** event: a string that specifies the name of the event. We already mentioned load and click events. For the curious, here's a full list of HTML DOM events.

> **Learning Note:** function: specifies the function to run when the event is detected. This is the magic that can allow your web pages to change dynamically.

For the event listener already written, we've added a handler for the 'click' event by providing a callback function. The callback function will be ```addTodo``` which we've written below.

**TASK** Use ```todoList```as the target for the eventlistener, and call the function that is passed in, ```deleteCheck```. This line should be exactly the same as line 8 except you are changing the target and function names.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

> **Learning Note:** If you right click on the web page and click ```inspect``` you can vist the console to interact with your app straight from the browser. 

> **Learning Note:** Chrome DevTools is a set of web developer tools built directly into the Google Chrome browser. DevTools can help you edit pages on-the-fly and diagnose problems quickly, which ultimately helps you build better websites, faster.

I created a callback function called ```addTodo``` which is passed to the event listener ```todoButton```. ```todoButton```should be clickable so when you click on it and checkout your console you see that some event is firing. Since the function isn't fully written we are seeing an error every time we click. Let's fix this.

<h2> Create an list element </h2>

First, we created a ```div``` that will contain a list. Then we've added a ```class``` to that ```div``` called ```todo```. So when this element is being generated, it will look like this ```<div class=todo></div>``` in HTML.
Everytime a todo is created from the input form, we want to create a list. For this we are going to create a new ```li``` element everytime a todo is created.
> **Learning Note:** ```li``` is list item in HTML.

**TASK:** Under the comment that says ```create the li element``` on line 18,create a ```const ```variable with the name ```newTodo``` equal to the createElement method to create a ```li``` item. This line will exactly the same as line 16. The only changes will be the name of the ```const``` variable and the element being passed to ```createElement``` will be ```"li"```.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

---

Each of these todo items will consist of the text that was inputted from the form. To grab that value we have to use the value of the ```todoInput```.

We then will add a class for the``` todo-item``` then append that new todo to the ```todoDiv```.

We create two buttons: a complete button and a delete button. Each time a new todo is created, a new complete button and a new delete button are created. When a new todo item is added to the ```div``` container, so are the two buttons.

<h2> Create the delete button </h2>

Each item in the todo list will have two buttons: a delete button, and a complete button. These buttons also consist of icons from the fontawesome icon directory.

Each complete button with have a check mark icon and they will be assigned a class called ```complete-btn```. Then we add it to the ```todoDiv```.

**TASK:** Now, we want to do the same thing for the delete button. First, create a button element for the delete button (it will be the same way the complete button is written on line 23 except call this ```const deleteButton```).

Then we add an icon to each delete button (which is already done for you).

**TASK:** Next, assign a class for each delete button. Do this under the comment that says ```"add a new class to the delete button"```. This line of code will look exactly the same as line 25 except you will use ```deleteBtn``` and you will ```add("delete-btn");```.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

Once the todo item is apart of the list, we can clear the input value from the form.

This is the ```addTodo``` function!

<h2> deleteCheck function </h2>

If you check out the Todo list in your browser, you'll notice it's partly working. We can create a todo, but we can't delete it or mark it as complete. That's what we'll work on now.

<h2> Giving the delete button functionality</h2>

**TASK:** Let's get the delete button working. Right now you see some code that is commented out (lines with ```//``` before them). Go ahead and uncomment the first line right beneath the ```deleteCheck``` function to the bracket under ```todo.remove()``` lines 39-43. To uncomment highlight those lines and use the shortcut ```cmd + /```. Save this and go back to your browser to check out the Todo list.

When you click on the trash can, a todo is deleted. 

**TASK:** Let's give that delete button some color. Go to the ```style.css``` file and go down to the selector for ```.delete-btn, .complete-btn```. We are going to add a ```background``` element and add ```border``` element here. Choose a color for the background (remember this can be a HEX value from the color picker with the ```#``` before the value) and for the border add ```border: none;```. The border will get rid of the black lines around the button elements. 

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

Now, let's get the completed button working!

<h2> Giving the completed button functionality </h2>

The completed button is going to be very similar to the delete button. 

**TASK:** The code you are going to write is going to check the first item in the classList array for the ```complete-btn``` class then you will assign a ```const todo``` to the parentElement of that item. Then we will ```toggle``` the ```completed``` element which is defined in our css. 

**HINT:** For this piece of code write the exact ```if``` statement for the ```delete-btn```. You will follow lines 39-43 exactly, but instead of ```'delete-btn'``` you will use ```'complete-btn'```. Instead of typing ```todo.remove()``` you will type in ```todo.classList.toggle('completed');```.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

> **Learning Note:** The toggle method toggles between adding and removing one or more class names from the selected elements. This method checks each element for the specified class names. The class names are added if missing, and removed if already set - This creates a toggle effect.

<h2> Makes CSS changes for our butoons </h2>

Now let's add some elements to our CSS file.

**TASK:** Go down to the ```.completed``` selector and add ```text-decoration: line-through;```.

Now when you check out the app in your browser and click the completed button, you will see that item has a line through it. Let's add one more element to our CSS property.

**TASK:**  Add ```opacity: 0.5;``` to the ```.completed``` class. 

Now when you click the completed button, the item has a line throught it and the opacity changes.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

This is all the code we will write for this project. Congrats on completing the coding exercise!! Now let's add our project to CircleCI!!

<h2>CircleCI</h2>
Something we haven't done yet is add our project to CircleCI. We were using version control to continuously integrate changes to GitHub but we didn't have CircleCI running. Let's do that before we start writing some tests. 

Let's complete the config file. If you look under the ```.circleci``` folder you'll see the ```config.yml``` file.

In this file, we are going to be adding an orb, and we will fill out some job info. 

We can see that we are using the Docker executor for our build job. This job is checking out our code from GitHub and running ```npm install``` to add some dependencies. 

In the deploy job we'll specify a machine to work on. In this case we are using the docker executor again, because that is the easiest machine to work with for our use case. Then Netlify calls the specified command in the docker executor so we can deploy to Netlify. We'll add this environment variable later.

For our workflow we call our build job, we run three test jobs that will test our code across different versions of node. 

<h2> Test our code against another version of node </h2>

**TASK** Add one more ```node/test``` job for version ```10.19.0``` and name the job ```test3```. Also, make sure it requires build like the other ```node/test``` jobs. This job will look exactly the same as ```test1``` and ```test2```. The only change will be the ```version``` of node you are testing against. 

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

We then have our jobs for deploying to Netlify and the only branch we'll deploy is the main branch.

The last job is for running our Cypress tests.

> **Learning Note** Cypress is a next generation front end testing tool built for the modern web.

> **Learning Note** First: Cypress helps you set up and start writing tests every day while you build your application locally. 
Later: After building up a suite of tests and integrating Cypress with your CI Provider, our Dashboard Service can record your test runs. You’ll never have to wonder: Why did this fail?

Let's make sure our config file deploys to Netlify before we begin writing our Cypress tests.

<h2> Create a Netlify account </h2>

You should have created your Netlify account during the pre-work.

Once you've signed up, you are going to create a "new site from Git". Connect your GitHub account, and choose the Todo list project from the list of repos.

Go to ```site settings``` > ```build and deploy``` > ```add a build hook``` > copy the url. This url is going to help us deploy to Netlify using CircleCI. Now, go to CircleCI. 

Go to the project settings of the project and click on environment variables. You are going to create an environment variable. Name the variable ```hook``` and add the url for the value.

Go back to your config, and add the variable ```hook``` between the ```${}``` so it should look like ```${hook}```. Now, we can deploy our project to Netlify via CircleCI.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push
CircleCI should be successful and you should be able to view your app live. 

You can find the url for where your project lives if you go to your Netlify project and click on the link at the top. The url should look like ```https://priceless-johnson-edbe3b.netlify.app```.

Congrats! You now have an application running on the web. 

The last thing we need to do is add some Cypress tests. We don't want to write the YAML for Cypress in our config file so let's add the Cypress orb.

Add [this](https://circleci.com/developer/orbs/orb/cypress-io/cypress) Cypress orb to the ```orbs``` key in the config file. It should look similar to the node orb.

<h2> Install Cypress </h2>

To [install Cypress](https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements) type this into your terminal (within your project directory)

    $ npm install cypress --save-dev

Cypress should be installed, and you should see a Cypress folder within your project now.

Now, create a ```cypress.json``` file and add your ProjectID to that file. The projectID should be available on the projects page in Cypress.

Let's add some tests to our project now.

Navigate to the ```integration``` folder within the ```Cypress``` folder, and delete all the files except ```sample_spec.js```. Open the ```sample_spec.js``` file in VScode. 

You'll see a couple of the tests that I've written. The first test will visit the Netlify website to make sure it is up and running.

**TASK:** Where you see ```visit``` for each test add the url for your app between the ```('')``` for each test.

**TASK:** The test you will write will check the Todo list to see if it contains the ```<h1>``` header you created in your HTML file. For instance, the header on my app says "My Todo List", so my test would look like:

    describe('My Second Test', () => {
        it('finds the content "type"', () => {
        cy.visit('https://priceless-johnson-edbe3b.netlify.app')
    
        cy.contains("My Todo List")
        })
    })


Let's make sure our CircelCI config is ready before we push to GitHub.

Go ahead and uncomment (hightlight the lines and use ```cmd + /``` to uncomment) the last section for the ```cypress/run``` job. This job will help us with running our tests by using the Cypress orb. We will record these tests, and store them as artifacts in CircleCI.

Add your changes to GitHub:

    1. git add .
    2. git commit -m "create a description here"
    3. git push

 Once you do this, everything should pass. Check out the CircleCI artifacts for the recordings of the Cypress tests. 

Congrats on finishing this project!

In this coding tutorial, learned how to:

* Use the command line
* Create and manipulate directories and files through the Terminal
* Commit and push changes to GitHub from the command line
* Write HTML/CSS/JavaScript
* Add the project to CircleCI, and add to the CircleCI config file
* Create an environment variable
* Push your application to Netlify
* Create tests with Cypress
* Store test recordings as artifacts in CircleCI

Hopefully, you have a better understanding of how teams use Git, GitHub, CircleCI, and testing tools. Of course things can get much more complicated than what we've seen in this tutorial, but I hope this has given you better insight into how teams operate with these tools.


