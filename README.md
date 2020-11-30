# I Wanna Show You (IWSY)

_**IWSY**_ is a presentation engine that runs in the browser. It's a single JavaScript file of about 40KB (unminified) that takes a JSON script and runs presentations (slide shows) with various transitions and effects, most notably the Ken Burns. Presentations can run in any designated `DIV` component or full-screen.

This project comprises the _**IWSY**_ engine plus an IDE that also runs in the browser and facilitates the creation of JSON presentations in an interactive manner.  All the project documentation is included in the IDE, so it must be hosted somewhere. You can choose static hosting, in which case all data will be saved into browser storage, or dynamic hosting, which uses a small REST server to access the host for file storage. The server is included, both as a PHP and as a Python script.
