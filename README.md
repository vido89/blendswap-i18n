# Blend Swap Internationalization Project

Internationalization files for the Blend Swap website, community built.

We need help with 

* Portuguese
* More languages? mainly left-to-right written langs.

We're covered in __Spanish__, __German__, __Polish__, __French__.

## Set up

### Requirements

* You will need a Github account and a basic knowledge of how to use Git for version control.
* [Fork](https://help.github.com/articles/fork-a-repo) this project.
* Download and install [PoEdit](http://www.poedit.net)
* Clone the full source files to your computer (you must [setup your ssh keys](https://help.github.com/articles/generating-ssh-keys) on Github for cloning and pushing code).

### Translating
* Let's say you will work with *Catalan*. In the sources root you will make this folder structure `cat/LC_MESSAGES` (if it doesn't exist already). The name of the *cat* folder is given by the three-character language codes in [ISO639-2 Standard](http://www.loc.gov/standards/iso639-2/php/code_list.php). The *LC_MESSAGES* subdir MUST HAVE THAT NAME. Take the Spanish translation as an example of the file structure.
* Open PoEdit for the first time it and enter your name and email when asked to. This is to keep a backlog of who commits what translations.
* From the PoEdit menu select *File > New Catalog from POT file*. browse for the `default.pot` file in the sources root folder and open it.
* You will be promted for the information of the translation.
    Enter the following:
    * Project name and version: Blend Swap Translation 0.1
    * Team: Blend Swap Translators
    * Team's email address: <your email address>
    * Language: Catalan
    * Country: SPAIN
    * Charset: UTF-8
    * Source code charset: utf-8
    * Plural forms: nplurals=2; plural=n == 1 ? 0 : 1;
* Hit *Accept*. Your Catalan catalog is created.
* Save the file to the folder you created before as default.po (watch out for the extension, POT files are templates, PO files are translations files).
* Work on your translations and save frequently. __you can use any UTF-8 compliant alphabet, which include [most character sets known to mankind](http://en.wikipedia.org/wiki/List_of_Unicode_Characters).__
* When you're done do your normal `git add .` , `git commit -m "Commit message"` and `git push` to update your fork of the translation files.
* When you feel your translation is ready, do a pull request on github to let poifox know it's time to merge your translation with our master fork.
* Do not use other software than poedit to edit the po files as it is very easy to break them, use PoEdit every time.

### What NOT to translate:

* the word Blend, use your language's plural forms if you like, but keep it as blend, as not everything is a single type of asset (eg. ITALIAN: blend &amp blendi <= that's ok with us.).
* `%s`, `%d`, etc. These are placeholders for things that are replaced on runtime. put them where they make sense.

### New strings.

From time to time new strings will be added to the translation files. When this is the case our commits will say so. when you see new strings have been pushed up the server do the following:

* Synchronize your master branch with our master byt making yourself a pull request from the main fork to yours.
* Open `your_lang_code/LC_MESSAGES/default.po` file with PoEdit and from the app menu select: __Catalog > Update from POT file__, browse for the default.pot file in the source root and accept it.
* The new strings will be listed. Hit accept to update your Catalan `default.po` file.
* Depending on your PoEdit settings some strings may be translated automatically; they appear yellowinsh, __YOU MUST ALWAYS DOUBLE CHECK THOSE STRINGS BECAUSE YOU CAN NEVER TRUST THOSE TRANSLATIONS__.
* Go back to translating as usual.

### Notes.

* The entire workflow applies to *lang/LC_MESSAGES/default.po* and *lang/LC_MESSAGES/model_validation.po* the other translation template files can be ignored for now.
* __DO NOT__ edit other files not pertinent to your language. the pot files in the root, the README and everything else that's not yours you should never EVER touch.
* We plan to update contributed translations at least once a week. Translating all these string doesn't take that long and it can be all done in a quick afternoon.
* PROTIP: when translating in PoEdit click on the first string, translate it and hit [ CTRL + DOWN ARROW ] the next string will be selected and you can type right away. This way you won't get tired of alternating between the mouse and the keyboard.
* The .mo files created by PoEdit are welcome, add them to your repo and leave them there, they contain the translations in binary form.
* __Do not use other software than poedit to edit the po files as it is very easy to break them, use PoEdit every time.__