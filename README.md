#touchstone

> ***noun*** 

> a standard or criterion by which something is judged or recognized.

> ***Synonyms*** - 

> standard, measure, model, pattern.

<hr />
Welcome to the LeanKit style guide. This repo is evolving quickly - expect change (especially as we add new bits/tools).

We've spent a good deal of time reviewing various portions of our code base in depth in hopes to come away with a set of core principles we can adhere to which can help alleviate any unnecessary cognitive overhead.

Our current goals/objectives:

* Establish a consistent approach to formatting
* Automate linting and formatting as much as humanly possible
* Commits/PRs from here on need to adhere to these guidelines (this include old code that is revisited/refactored, etc.)

This document is young, and we're going to focus on JavaScript initially. 

##JavaScript

###Supported IDEs
We're standardizing on Sublime Text 3 and Visual Studio (currently 2013). Seriously, ST3 is highly preferred for JS development. Visual Studio is included because we obviously have a significant amount of .NET code, and context-switching between IDEs to work on files in the same solution isn't a fair thing to ask of anyone!

> But....I LOVE WebStorm!

Actually, me too. But the goal here is to gain the efficiencies that come from adopting standards and automating the minutiae. There are lots of tools for both ST3 and VS that we'll be able to take advantage of - but many other tools will be developed over time by our team. Focusing on these two IDEs means we get better quality tooling and we don't lose the efficiency gains by supporting other IDEs.

See the "IDE Setup" sections for more information on plugins/extensions you need to have installed.

###Linting
Under `linting/JavaScript`, there are four folders: `node`, `specs`, `webclient` and `VisualStudio`. Each one contains a `.jshintrc` file tuned for those specific cases (specs should work for our mocah + should tests in both node and browser). These jshint configurations are the standard - please do not alter them locally within a project. All PRs will be linted (this will eventually be automatic), so changing a setting locally will likely result in a rejected PR.

The Visual Studio `.jshintrc` file is intended to be used with the Web Essentials extension. See the section on "IDE Setup" for more info.

###Formatting
The js-beautify settings file for Sublime Text 3 is included in `linting/JavaScript/JavascriptBeautify.sublime-settings`. You will need to copy and paste the contents of this file into your local ST3 settings by doing the following:

* In Sublime Text, navigate to Preferences -> Package Settings -> JavaScript Beautify -> Settings User
* Copy the contents of the file in this repo into your user settings file.
* Save and close.

The Visual Studio formatting settings require ReSharper - see the "IDE Setup" section for more info.

##IDE Setup

###Sublime Text 3

###Visual Studio 2013