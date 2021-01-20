<h2> Install node and npm </h2> 

We need to install node on our computers so we have access to npm, which will let us install Cypress. 

In your terminal type

    $ brew install node

Check to make sure node was installed by typing

    $ node -v

Check to make sure npm was installed by typing

    $ npm -v

Go to [] and clone the todo list project. 

To clone the project, go to ```code``` button on the repo page, and copy the url for ssh.

Open up your terminal, and check which directory you are in with the command ```pwd```.

You should be in the ```projects``` directory. If you aren't, and you are in your home directory (```/Users/radhika```) then type in the command ```ls``` to see the list of directories you can access.

You should see the ```projects``` directory, and you can use the command ```cd projects``` to access this directory.

Now that you are in ```projects``` make sure the url from GitHub is copied and type the command ```git clone [url]``` (when typing in the ssh url don't use the brackets).

Once you've cloned the project, you should see it in your projects folder. Type the command ```ls``` to list your files. 

<h2> Add project to GitHub </h2>
Let's create the GitHub repo before we get started.

To add the project to GitHub, check out the GitHub tutorial and follow the instructions to create the repo.

Then type the command ```cd todolist``` to access the project. 

Now, you are in the project directory. Let's open this project within our text editor. Remember, if you are using vscode, you can type the command ```code .``` within your terminal and open the project from there.

Once you've opened the project, let's take a look at what it looks like on a web page. If you are using vscode, right click in the html file and choose ```open in live server```. When you do this, the file will open up in your browser and you should see see a web page. You'll notice the web page is not complete, but that's what we'll work on! You can check out the video below to see what we are working towards.

If you go back to the text editor, you'll see a list of files. Let's go through these files and take a look at each one.

Let's first take a look at the ```index.html``` file. This is the html file for the project.

> HTML (HyperText Markup Language) is the standard markup language for creating Web pages. Markup languages are languages used by a computer to annotate a document. Markup languages define the style and structure of a document so that a computer knows how you want that document to appear.

An HTML element is defined by a start tag, some content, and an end tag. If we look at the HTML file in our text editor, we see this in action. 

The first couple of lines in the file are ```<!DOCTYPE html> <html lang="en">```. A doctype or document type declaration is an instruction which tells the web browser about the markup language in which the current page is written. The Doctype is not an element or tag, it lets the browser know about the version of or standard of HTML or any other markup language that is being used in the document. In the case of our file, we are using HTML 5.

> The ```lang``` attribute specifies the language of the element's content. Common examples are "en" for English, "es" for Spanish, "fr" for French and so on.

> The ```charset``` attribute specifies the character encoding for the HTML document.

> The HTML5 specification encourages web developers to use the UTF-8 character set, which covers almost all of the characters and symbols in the world!

> The ```rel``` attribute specifies the relationship between the current document and the linked document/resource.

> The ```href``` attribute specifies the URL of the page the link goes to.

In this html document, the ```<head>``` tag

The ```<head>``` element is a container for metadata (data about data) and is placed between the ```<html>``` tag and the ```<body>``` tag.

Metadata is data about the HTML document. Metadata is not displayed.

Metadata typically define the document title, character set, styles, scripts, and other meta information.

The ```<title>``` tag defines the title of the document. The title must be text-only, and it is shown in the browser's title bar or in the page's tab.

The ```<body>``` tag defines the document's body.

The ```<body>``` element contains all the contents of an HTML document, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

Within the ```<body>``` tags in this html file, we have other tags that make up our web page.

<h2> First Assignment</h2>

The first assignment you need to do is create an ```<h1></h1>``` tag under the header tag in the html document. Within the ```<h1></h1>``` tag you will create the name of your project. This project is a Todo list, so you can name it "My Todo List" or something like that. [Here](https://www.w3schools.com/tags/tag_hn.asp) is an example of how to use the ```h1``` tag.

Once you've added your ```h1``` tag, open up this file in the live server again, and you should see the header on the web page.

> 127.0.0.1 is the loopback Internet protocol (IP) address also referred to as the localhost. The address is used to establish an IP connection to the same machine or computer being used by the end-user. When making network requests, you use an IP address, or a host name, and a port. For example we might have a web server running on our machine. A second web server can be started on a different port.

The next tag we'll look at in the html file is the ```<form>``` tag. 

> The ```<form>``` tag is used to create an HTML form for user input.

<h2> Second Assignment </h2>

The ```input``` tag is used to specify an input field where the user can enter data. We need to create an HTML element for the input. To do this you are going to use the ```<input>``` tag. The ```type``` for this ```input``` tag is ```text```. Then you will also add a class of ```"todo-input```. Check out [this](https://www.w3schools.com/w3css/w3css_input.asp) example to get an idea of how to use the input tag.

Now check out the web page in your browser. You should see an input form now! If you try and type something in it, the text won't get processed just yet. 

The rest of the html file is filled out for you. 

Underneath the input, we see a button. The button is the right next to the input form on the webpage. 

> The class attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.

> The button tag has a type of submit. The type attribute specifies the type of button.

Within the button tag, there is an ```span``` tag.

> The HTML ```<span>``` tag is used for grouping and applying styles to inline elements.

The ```span``` tag is being used to display an icon. The icons are coming from the [font awesome](https://fontawesome.com/) website. We are importing the icons in the html file at the top of the file.

Once we close out the ```form``` tag, we create a ```div```.

> The ```<div>``` tag defines a division or a section in an HTML document. It is used as a container for HTML elements - which is then styled with CSS or manipulated with JavaScript. The ```<div>``` tag is easily styled by using the class or id attribute.

With the ```div``` tag in our html file, we created a ```div``` for the todos that will list out once they are added on the webpage. We can style this container or section on our html page through CSS.

Right before we close out the html page, we add a ```script``` tag to link to our Javascript. Before we dive into the Javascript, let's look at our CSS file first.

<h2> CSS File </h2>

Open the CSS file ```style.css```. 

> Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS describes how elements should be rendered on screen, on paper, in speech, or on other media. CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

> HTML was NEVER intended to contain tags for formatting a web page. HTML was created to describe the content of a web page. When tags like ```<font>```, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process. To solve this problem, the World Wide Web Consortium (W3C) created CSS. CSS removed the style formatting from the HTML page.

A CSS rule-set consists of a selector and a declaration block. The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

The first css block begins with the ```body``` selector. By selecting the ```body``` you are selecting the entirety of the html document and assigning CSS to the entire document.

As we go down the CSS file, we have more selectors and we are applying styles to these selectors. 

Let's make a couple of changes to this file.

<h2> Third Assignemnt </h3>

Add a ```background-color``` or ```background-image``` tag under the comment. You can use [this](https://htmlcolorcodes.com/) color picket to find a hex value for the ```background-color```. **Don't forget the ```#``` before the hex value.**  If you would like to use a ```background-image``` this is a little more complicated. You can take a look at the examples [here](https://www.w3schools.com/cssref/pr_background-image.asp) if you are interested.

<h2> Third Assignemnt </h2>
On the web page, you will notice a button with a square. This is the button that will submit a todo item and a list will be created. Let's add some color to this button.

Under the form button selector add the ```color``` attribute, and add a hex value like ```#E29178``` as the value.

When you refresh the page, you'll see that the button has color. The color changes as you hover over the button because of the ```form button:hover``` selector.

We'll come back to the CSS once we've added some Javascript.

<h2> Javascript </h2>
JavaScript is a text-based programming language used both on the client-side and server-side that allows you to make web pages interactive. Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user. Common examples of JavaScript that you might use every day include the search box on Amazon, a news recap video embedded on The New York Times, or refreshing your Twitter feed.  

>The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page. A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.


For this project, we are using vanilla Javascript, but you can use different frameworks like ReactJS, VueJS, etc for different frontend JS frameworks or a framework like Node for backend programming. Both Node.js and React.js are JavaScript frameworks but they are entirely different concepts. The most significant difference between Node.js and React.js is React is used to create user applications, while Node.js is a back-end system. 

Let's take a look at the ```app.js``` file.

We start off by creating a variable with ```const``` and setting them equal to specific elements. 

> The method querySelector() returns the first Element within the document that matches the specified selector, or group of selectors.

> Variables defined with ```const``` behave like ```let``` variables, except they cannot be reassigned.

<h2> Fourth Assignemnt </h2>

```const todoInput``` and ```const todoButton``` are set to the form input and button elements.

We need to create a const variable for the ```todo-list``` as well. Go ahead and create another querySelector for the ```todo-list``` element. The const variable should be ```todoList```.

The next section of the Javascript is for the event listeners.

The ```addEventListener()``` method attaches an event handler to the specified element.

> Events are actions that happen when the user or browser manipulates a page. They play an important role as they can cause elements of a web page to change dynamically.

> For example, when the browser finishes loading a document, then a load event occurred. If a user clicks a button on a page, then a click event has happened.

> Many events can happen once, multiple times, or never. You also may not know when an event will happen, especially if it is user generated.

> In these scenarios, you need an event handler to detect when an event happens. This way, you can set up code to react to events as they happen on the fly.

>JavaScript provides an event handler in the form of the addEventListener() method. This handler can be attached to a specific HTML element you wish to monitor events for, and the element can have more than one handler attached.

In our case, we need event listeners to **add a todo**, and to **remove a todo**.  

I've already added an addEventListener for adding a todo. We need one for removing an item. 

The syntax for the eventlistener method is 

```target.addEventListener(event, function, useCapture)```

> target: the HTML element you wish to add your event handler to. This element exists as part of the Document Object Model (DOM) and you may wish to learn about how to select a DOM element.

> event: a string that specifies the name of the event. We already mentioned load and click events. For the curious, here's a full list of HTML DOM events.

> function: specifies the function to run when the event is detected. This is the magic that can allow your web pages to change dynamically.

For the event listener already written, we've added a handler for the 'click' event by providing a callback function. The callback function will be ```addTodo``` which we've written below.

Use the ```todoList```const variable to add the eventlistener to and call the function that is passed in, ```deleteCheck```.

If you right click on the web page and click ```inspect``` you can vist the console to interact with your app straight from the browser. 

> Chrome DevTools is a set of web developer tools built directly into the Google Chrome browser. DevTools can help you edit pages on-the-fly and diagnose problems quickly, which ultimately helps you build better websites, faster.

Let's make sure that we are reciving some feedback from out submit button. We want to see that when we click it, we see that an event if being triggered.

I created a callback function called ```addTodo``` which is passed to the event listener ```todoButton```. ```todoButton```should be clickable so when you click on it and checkout your console you see that some even is firing. Since the function isn't fully written we are seeing an error every time we click. Let's fix this.

<h2> Fifith Assignemnt </h2>

First, we created a div that will contain a list. Then we've added a class to that div called ```todo```. So when this element is being generated, it will look like ```<div class=todo></div>```
Everytime a todo is created from the input form, we want to create a list. For this we are going to create a new ```li``` element everytime a todo is created.
> ```li``` is list item in html.

Under the comment that says ```create the li element``` create a const variable equal to the createElement method to create an ```li``` item.


Each of these todo items will consist of the text that was inputted from the form. To grab that value we have to use the value of the ```todoInput```.

We then will add a class for the``` todo-item``` then append that new todo to the ```todoDiv```.

For the buttons we created two buttons with class names then we’ve appended each button to the ```todoDiv```.

<h2> Sixth Assignemnt </h2>

Each item in the todo list will have two buttons: a delete button, and complete button. These buttons also consist of icons from the fontawesome icon directory.

Each complete button will be a button. Each button will have a check mark icon and they will be assigned a class called ```complete-btn```. Then we add it to the ```todoDiv```.

Now, we want to do the same thing for the delete button. First, create a button element for the delete button (it will be the same way the complete button is written except call this ```const deleteButton```).

Then we add an icon to each delete button.

Next, create assign a class for each button. Do this under the comment that says ```"add a new class to the delete button"```.

Once the todo item is apart of the list, we can clear the input value from the form.

This is the addTodo function!

<h2> deleteCheck function </h2>

If you check out the Todo list in your browser, you'll notice it's partly working. We can create a todo, but we can't delete it or mark it as complete. That's what we'll work on now.

<h2> Seventh Assignemnt </h2>

Let's get the delete button working. Right now you see some code that is commented out. Go ahead and uncomment lines 47-50 by highlighting those lines and using ```cmd + /```. Save this and go back to your browswer to check out the Todo list.

When you click on the trash can, a todo is deleted. 

Let's give that button some color. Go to the ```style.css``` file and go down to the selector for ```.delete-btn, .complete-btn```. We are going to add a ```background``` element and a ```border``` element here. Choose a color for the background and for the border add ```border: none;```. The border got rid of the black lines around the elements. 

Now, let's get the completed button working!

<h2> Eighth Assignemnt </h2>

The completed button is going to be very similar to the delete button. The code you are going to write is going to check the 0th class for the ```complete-btn``` class then you will assign a ```const todo``` to the parentElement of that item. Then we will ```toggle``` the ```completed``` element which is defined in our css. 

HINT: For this piece of code write the exact ```if``` statement for the ```delete-btn``` but instead of ```'delete-btn'``` you will use ```'complete-btn'```.

Instead of typing ```todo.remove()``` you will type in ```todo.classList.toggle('completed');```.


> The toggle method toggles between adding and removing one or more class names from the selected elements. This method checks each element for the specified class names. The class names are added if missing, and removed if already set - This creates a toggle effect.

<h2> Ninth Assignemnt </h2>

Now let's quickly add some elements to our CSS file.

Go down to the ```.completed``` selector and add a ```text-decoration: line-through;```.

Now when you check out the app in your browser and click the completed button, you will see that item has a line through it. Let's add one more element to our CSS property.

Add ```opacity: 0.5;``` to the ```.completed``` class. 

Now when you click the completed button, the item has a line through and the opacity changes.

This is all the code we will write for this project. Congrats!!

<h2>CircleCI</h2>
Something we haven't done yet is add our project to CircleCI. We were using version control to continuously integrate changes to GitHub but we didn't have CircleCI running. Let's do that before we start writing some tests.

Let's complete the config file. If you look under the ```.circleci``` folder you'll see the ```config.yml``` file.

In this file, we are going to be adding a couple orbs, and we will fill out some job info. 

We can see that we are using the Docker executor for our build job. This job is checking out our code from GitHub and running npm install to add some dependencies. 

In the deploy job we'll specify a machine to work on, in this case we are using the docker executor again, because that is the easiest machine to work with for our use case. Then Netlify calls the specified command in the docker executor so we can deploy to Netlify. We'll add this environment variable later.

For our workflow we call our build job, and we then run three test jobs that will test our code across different versions of node. Honestly, this doesn't do much for our project because we aren't leveraging node but for demo purposes this is what it would look like if we did need to do this.

<h2> Tenth Assignemnt </h2>

Add one more ```node/test``` job for version ```10.19.0``` and name the job ```test3```.

We then have our jobs for deploying to netflify and the only branch we'll deploy is the main branch.

The last job is for running our Cypress tests.

> Cypress is a next generation front end testing tool built for the modern web.

> First: Cypress helps you set up and start writing tests every day while you build your application locally. 
Later: After building up a suite of tests and integrating Cypress with your CI Provider, our Dashboard Service can record your test runs. You’ll never have to wonder: Why did this fail?

Let's make sure our config file deploys to Netflify before we begin writing our Cypress tests.

<h2> Create a Netlify account </h2>

First, you are going to create a [Netlify](https://www.netlify.com/) account. Sign up with GitHub.

Once you've signed up, you are going to create a "new site from Git". Connect your GitHub account, and choose the Todo list project from the list of repos.

Go to ```site settings``` > ```build and deploy``` > ```add a build hook``` > copy the url

This url is going to help us deploy to Netlify using CircleCI. Now, go to CircleCI. 

Go to the project settings of the project and go to environment variables. 

You are going to create an environment variable. Name the variable ```hook``` and add the url for the value.

Go back to your config, and add the variable ```hook``` between the ```${}``` so it should look like ```${hook}```. Now, we can deploy our project to Netlify via CircleCI.

Go ahead and add your changes to GitHub. CircleCI should be successful and you should be able to view your app live. 

You can find the url for where your project lives if you go to your Netlify project and click on the link at the top. If should looks like ```https://priceless-johnson-edbe3b.netlify.app```.

Congrats! You now have an application running on the web. 

The last thing we need to do is add some Cypress tests. We don't want to write the YAML for Cypress in our config file so let's add the Cypress orb.

Go to the [orbs page](https://circleci.com/developer/orbs?utm_source=gb&utm_medium=SEM&utm_campaign=SEM-gb-200-Eng-ni&utm_content=SEM-gb-200-Eng-ni-CircleCI-Orbs&utm_term=OrbRegistryLP&gclid=CjwKCAiAo5qABhBdEiwAOtGmbpVpBx2scJrXD-jErRj8YnhE6s9fDhSxWPcCMDOrVbR1dw4Z27Gj8hoCdI4QAvD_BwE) and find the Cypress orb.

Add it under the ```orbs``` key in the config file. 


<h2> Install Cypress </h2>

To [install Cypress](https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements) type this into your terminal (within your project directory)

    $ npm install cypress --save-dev

Cypress should be installed, and you should see a Cypress folder within your project now.

Now, create a ```cypress.json``` file and add your ProjectID to that file.

Let's add some tests to our project now.

Naviage to the ```integration``` folder within the ```Cypress``` folder. Open the ```sample_spec.js``` file in your code editor. 

You'll see a couple of the tests that I've written. The first test will visit the Netlify website to make sure it is up and running.

Where you see ```visit``` add the url for your app between the ```('')``` for each test.

The test you will write will to be if the Todo list contains the ```<h1>``` header you created in your HTML. For instance, the header on my app sayd "My Todo List".

Use [this](https://docs.cypress.io/api/commands/contains.html#Syntax) doc to help with writing the test (it should be exactly the same as the other tests).

Let's make sure our CircelCI config is ready before we push to GitHub.

Go ahead and uncomment the last section for the ```cypress/run``` job. This job will help us with running our tests by using the Cypress orb. We will record these tests, and store them as artifacts in CircleCI.

Go ahead and push to GitHub. Once you do this, everything should pass. Check out the CircleCI artifacts for the recordings of the Cypress tests. 

Congrats on finishing this project!

