# Symfony2 documentation ePub

Has the following crossed your mind?

>>> "I would like to read Symfony2 documentation on my e-reader..."

This repository contains a very crude ePub (tested on Kobo) which you can download if you are lazy. But if you yearn for a better version, the following instructions _might_ help you to get started (tested on OS X, Mountain Lion).

1. ```git clone git://github.com/symfony/symfony-docs.git```
2. ```sudo easy_install -U sphinx``` (assuming you have the necessary Python stuff)
3. Go to the ```symfony-docs``` directory
4. ```mv index.rst index-original.rst``
5. Run ```sphinx-quickstart```. Hit enter until there's a question about ePub. Answer ```y```.
6. ```mv index-original.rst index.rst``` (replace the generated index with the original)

You can also replace the created ```conf.py``` with the one supplied in this repository (uses epub theme).

7. Install extensions [http://symfony.com/doc/current/contributing/documentation/format.html#installing-the-sphinx-extensions](http://symfony.com/doc/current/contributing/documentation/format.html#installing-the-sphinx-extensions)
8. ```make singlehtml```. You can also try ```make epub``` but I had no success with it
9. Import the generated ```index.html``` from ```_build/singlehtml``` directory in [Calibre](http://calibre-ebook.com) and export it to ePub

Obs. the export process might take some time (17 minutes for Quick Start, Book and Cook Book on my computer). I suggest that you only generate the quick start first to see how long it takes. You can do this by removing other elements from ```index.rst```.

## TODO

Fix the following:

- PHP syntax highlighting
- First pages (including cover)
- TOC
- ?