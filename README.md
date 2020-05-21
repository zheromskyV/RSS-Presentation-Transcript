# RSS-Presentation-Transcript

Link to the presentation: https://zheromskyv-presentation.netlify.app/#/

## Slide 1
### Electron
Electron is a framework for building cross-platform desktop apps using nothing but JavaScript, HTML, and CSS.

## Slide 2
### History
The journey of Electron started in January 2013 by engineer at GitHub Cheng Zhao with the search for a tool to build a cross-platform text editor on which the user can work with technologies like JavaScript, HTML, and CSS. It was initially known as Atom Shell.

In 2014 the project became open sourced. 

In 2015 the project was renamed to Electron. 

And in 2016 Electron 1.0 was released as a platform for building desktop apps with web-technologies.

## Slide 3
### Apps built with Electron
Today this is the tool behind many popular apps you might be using every day.

Such apps as Visual Studio Code, Atom, Slack, Twitch, Discord and many-many others were created using Electron.

Thousands of organizations spanning all industries use Electron to build cross-platform software.

And why is it so popular?

## Slide 4
### It's even easier than you think
As was said, Electron allows to create native applications with web technologies. It means that if you can build a website, you can build a desktop app. Electron takes care of the hard parts so you can focus on the core of your application.

## Slide 5
### Hard parts
Such things as updating, reporting, debugging, profiling are made easy for you. For instance, …
* AutoUpdater enables apps to automatically update themselves.
*	MenuClass creates native application menus and context menus.
*	CrushReporter submits crash reports to a remote server.
*	ContentTracer collects tracing data from Chromium to find performance bottlenecks and slow operations.
*	ElectronForge, GruntElectronInstaller generate a Window installer.
So, Electron takes care of all these hard and tedious parts of creating a desktop application so the user can focus on the core of his or her application.

## Slide 6
### How does it work?
On the front-end you build UI just like you would for a browser-based web-app and you can bring along to your favorite frameworks. You can use Angular, React, Vue, whatever you like. 

But in the electron you also have access to NodeJS. That means you can access low-level APIs that you don`t normally have access to in a browser like the file system.

## Slide 7
Electron combines the front-end and back-end technologies and provides a bunch of other tools to work with native menus, the system tray and so on. Electron combines Chromium and NodeJS into a single runtime. That`s what enables us to run the HTML, CSS and JavaScript code as a desktop application.

## Slide 8
Electron applications have two mandatory processes, the main process, and the rendering process. 

Each process has a different role to enact. 

Bootstrapping the application is performed by the main process. It can withstand other application lifecycle events like starting up, quitting, preparing to quit and other lightweight tasks like going to the background and coming to the foreground. 

On the other hand, the rendering process is spawned by the main process. The render processes will display the UI of the application. Each process takes advantage of Chromium’s multiprocess architecture and runs on its own thread.

## Slide 9
To put it simply, The purpose of the main process is to create web pages using a BrowserWindow Instance. The BrowserWindow Instance uses a renderer process to run each web page.

Each app can have only one main process but can have many renderer processes.

It is possible to communicate between the main and the renderer process as well.

## Slide 10
### Electron App Example
Let's see how fast and easy it is to use Electron on a small example. 

Our app will consist of html file with markdown, css file with styles and js file with scripts. Render.js file will be completely empty – it's just recommended by the documentation to have it.

## Slide 11
Firstly, we need to install electron: 
* `npm install -g electron` – install globally;
* `npm install electron -save` – install locally;
* `electon .` – run the project.

## Slide 12
In main.js we need to include some modules. The first one is `path` which let us work with paths to our files and directories. The second one is `url` which provides utilities for URL resolution and parsing. And finally, from the Electron we import such things as app and BrowserWindow.

## Slide 13
Here we basically create a BrowserWindow Instance and load index.html into the BrowserWindow.

## Slide 14
This code snippet says that when the application is ready, load the first window.

Similarly, app can be used to perform other actions on various events. For example, it can be used to perform some action right before the application closes and so on.

## Slide 15
Here we create index.html file – our page:
1.	Create a text box with id `Celsius`. Whenever anything is typed in this textbox, the `celsiusToFahrenheit()` function is called.
2.	Create a text box with id `Fahrenheit`. Whenever anything is typed in this textbox, the `fahrenheitToCelsius()` function is called.
3.	So, whenever a new value is typed in the Celsius text box, the value in the Fahrenheit text box displays the same temperature in Fahrenheit and otherwise.

## Slide 16
Then we need to add the script into our html. `Render.js` file is required. And right here we can write our functions.

The `celsiusToFahrenheit()` function reads the value in the Celsius text box, converts it to Fahrenheit, and writes the new temperature into the Fahrenheit text box. The `fahrenheitToCelsius()` function does the exact opposite of this.

## Slide 17
Run `electron .` and we have this application.

## Slide 18
We also have native menu with lots of options created for us and not by us.

## Slide 19
We also have Chrome Dev Tools. We can edit our code and use it just like we would in the browser.

## Slide 20
Some lines of css code 

## Slide 21
and we have nice looking app. That`s it!

## Slide 23
### Conclusion
Overall, Electron takes care of most of the dynamic applications which use our browser as a platform to deliver their embedded features and help developers connect with a wider audience. 

## Slide 24
Hope I`ve managed to shed some light on what Electron is. 

Thanks for your attention!
