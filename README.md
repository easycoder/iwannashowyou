# I Wanna Show You (IWSY)

_**IWSY**_ is a presentation engine that runs in the browser. It's a single JavaScript file of about 40KB (unminified) that takes a JSON script and runs presentations (slide shows) with various transitions and effects, most notably the Ken Burns. Presentations can run in any designated `DIV` component or full-screen.

This project comprises the _**IWSY**_ engine plus an IDE that also runs in the browser and facilitates the creation of JSON presentations in an interactive manner.  All the project documentation is included in the IDE, which can be hosted either on a server or a personal computer. You can choose static hosting, in which case all data will be saved into browser storage, or dynamic hosting, which uses a small REST server to access the host for file storage. The server is included, both as a PHP and as a Python script. The former is for servers and the latter for personal computers.

The _**IWSY**_ is pure JavaScript with no external dependencies. The IDE is coded entirely in _**EasyCoder**_ script, full documentation for which can be found at [https://easycoder.github.io](https://easycoder.github.io). Start with `index.html`; this contains a small boot script that loads `resources/ecs/iwsy.txt`, the main script for the IDE. _**EasyCoder**_ scripts are easy to read by anyone with some programming experience. The main JavaScript libraries and IDE scripts are loaded from CDN.

## How to use IWSY

There are 3 ways to use _**IWSY**_:

1. Directly from this repository, at [https://iwannashowyou.netlify.app](https://iwannashowyou.netlify.app). The site is hosted statically so all your data is stored in your browser, where it will remain available each time you revisit _**IWSY**_.
  
1. By copying all the files from the repository to any server, typically LAMP/WAMP/MAMP. If the server runs PHP your data can be stored on the server once you've set up a database (see below). If not then it will behave just as in (1) and store data in your browser.
  
1. By copying all the files from this repository to your computer. You will need Python3 installed. At the command line, navigate to the folder then type `py rest.py`, where the initial `py` is the command that launches Python3. Then go to your browser and type `localhost:17348` in the address bar (the port number is defined at the bottom of the `rest.py` script). All your data will be stored in a subfolder on your computer.

## User management

If you choose option (2) above with a PHP server the UI will show a Users button at the right-hand end of its toolbar. User data is stored in a database provided by you and its initialization parameters for the database are held in `resources/properties.txt`. If things don't work as expected you may need to study the code of the Users code module, at `resources/ecs/user.txt`, in particular the various `rest` commands used through the script, to discover where a mistake has occurred. There is also an email address hard-coded into the Users module, that you will want to change.
