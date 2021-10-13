## Keeping Libraries Straight with Virtual Environments
#### Cited from the book *Web Scraping with Python*

If you intend to work on multiple Python projects or you need a way to easily bundle
projects with all associated libraries, or you’re worried about potential conflicts
between installed libraries, you can install a Python virtual environment to keep
everything separated and easy to manage.

If you intend to work on multiple Python projects or you need a way to easily bundle
projects with all associated libraries, or you’re worried about potential conflicts
between installed libraries, you can install a Python virtual environment to keep
everything separated and easy to manage.

```$ virtualenv scrapingEnv```

This creates a new environment called scrapingEnv, which you must activate in order
to use:

```
$ cd scrapingEnv/
$ source bin/activate
```

After you have activated the environment, you will see that environment’s name in
your command line prompt, reminding you that you’re currently working with it.
Any libraries you install or scripts you run will be under that virtual environment
only.

Working in the newly-created scrapingEnv environment, I can install and use Beauti‐
fulSoup, for instance:

```
(scrapingEnv)ryan$ pip install beautifulsoup4
(scrapingEnv)ryan$ python
> from bs4 import BeautifulSoup
>
```

I can leave the environment with the deactivate command, after which I can no
longer access any libraries that were installed inside the virtual environment:

```
(scrapingEnv)ryan$ deactivate
ryan$ python
> from bs4 import BeautifulSoup
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
ImportError: No module named 'bs4'
```

Keeping all your libraries separated by project also makes it easy to zip up the entire
environment folder and send it to someone else. As long as they have the same ver‐
sion of Python installed on their machine, your code will work from the virtual envi‐
ronment without requiring them to install any libraries themselves.

Although we won’t explicitly instruct you to use a virtual environment in all of this
book’s examples, keep in mind that you can apply virtual environment any time sim‐
ply by activating it beforehand.
