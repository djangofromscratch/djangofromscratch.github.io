## Where does the application start?

The key to understand any kind of application is to know where does it start. Until then you'll keep banging your head, shooting in the dark and lastly, at the mercy of Google when trying to debug or solve any issues you have.

Majority of web developers don't really know, or even care where actually their application start. This particularly true for those developing in PHP which abstract most of the web parts and it appear to developer they just writing a regular command line or desktop application.

For Django developer, you can probably ignore this throughout your dev carrier but knowing it will help you a lot in.

Django application can start (at least) from 2 possible entry point. The first entry point is through the development server and the second entry point is when you deploy it to production web server, either mod_wsgi, gunicorn, Paste, Rocket, Waitress, Circus or dozen more WSGI server you can find on PyPI. I can still remember the day when there's none pure Python WSGI server exists (except CherryPy) and how I'd really envy Rails's community for having Mongrel. That day has long gone.

Let's dive to the first entry point - when you run your django application through the manage.py runserver command. Typical django application (as generated) by the startproject command has a file called manage.py at the root of the project directory. This is the file that developer use to interact with their application, doing things such as running development server, synching database tables with the models definition, loading/exporting data and so much more.

If you peek into manage.py, it's pretty simple actually:-
