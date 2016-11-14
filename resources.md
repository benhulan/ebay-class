# Coding 101 for Product Managers

#### Tools
- [Download Google Chrome HERE](https://www.google.com/chrome/browser/desktop/index.html?brand=CHBD&gclid=Cj0KEQiA9ZXBBRC29cPdu7yuvrQBEiQAhyQZ9A8Gkei2lG33_Ba4XuylJlT_TjITSP4mVHhwyHc20agaAiZ-8P8HAQ)
- [Download SublimeText3 HERE](https://www.sublimetext.com/3)
- [Join GitHub HERE](https://.github.com)



**We will be using github.com to track code and for collaboration.** The following instructions may be overkill, but if anyone has problems with system configuration, I think I've covered all the bases. (PC/Ubuntu users, you're on your own!)

In OSX you need the Command Line tools to run `git` commands from the Terminal.
Otherwise, you're doing everything on GitHub.com, which is ok, but it isn't as cool. 

### How to Install Command Line Tools from Terminal

1. Open the Terminal application.
2. In your Terminal, type `xcode-select --install`, and a new window and installer will appear. 
3. Follow the instructions in the installer. 

## Homebrew

<a href="http://brew.sh/" target="_new">Homebrew</a> is a *package manager* for OS X.  We'll use to quickly download and install other tools we use, or to update already-installed tools. 

1. Open the Terminal application, and run `which brew` to check if you have Homebrew installed already. The `which` Terminal command shows where on your computer a program is installed. If it is installed, the Terminal will output a file path. If it is not installed, the Terminal won't output anything.

2. **Only if you do not have Homebrew installed**, run the command below to install Homebrew. Wait while Homebrew downloads and installs.

    ```bash
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

    If you run into problems, you may need to run `rm -rf /usr/local/Cellar /usr/local/.git` and then retry the command above.

3. Run `brew update` to update Homebrew.

4. Run `brew doctor` in your Terminal to check that Homebrew and any current packages are installed correctly. If there are issues, `brew doctor` will list suggestions for how to fix them.  Follow these suggestions one by one. If you're not sure what to do, **ask!**

5. Based on the errors in the step above, you may need to edit your `~/.bash_profile` to include the path to Homebrew if `brew doctor` shows warnings.  If in doubt ask for help here.

    ```bash
    bash echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile
    ```

6. Let's install our first package with Homebrew, `tree`!  This package adds a command to your Terminal that displays files in a tree view (instead of a list view like `ls`).  Enter the following command in your Terminal:

    ```bash
    brew install tree
    ```

7. Run the Terminal command `tree` to see a tree view of all the files inside your current directory!


### Git

1. To check whether git is installed on your system, run the Terminal command `which git`. The output should be a directory path like `/usr/bin/git`; this is where git is installed on your machine.


2. **Only if you do not have git installed,** run the following command in your Terminal:

    ```
    brew install git
    ```

### Configure Git

Configuring your git settings to help GitHub track your contributions and to make it easier and smoother to commit. 

1. Use the following three `git config` commands to configure your git user information and have git "cache" (remember) it. We use the `--global` (or `-g`) option to make the configuration apply to all repositories.
  
    ```
    git config --global user.name "YOUR-USERNAME"
    git config --global user.email YOUR-EMAIL-ADDRESS
    git config --global credential.helper cache
    ```

1. Generate a SSH key for GitHub. This will allow you to use GitHub from your Terminal without entering your login information every time you push.

    <a href="https://help.github.com/articles/generating-an-ssh-key" target="_new">Generating SSH Keys (via GitHub.com)</a>


## SublimeText 3

__Optionally, you can install TextWrangler or Atom. Atom is a phenomenal IDE but I'll be using SublimeText3__

1. Use the following link to <a href="https://download.sublimetext.com/Sublime%20Text%20Build%203103.dmg">download Sublime Text 3 for Mac.)</a>. To install for another system go [here](https://www.sublimetext.com/3)

2. Open the downloaded file.

3. Follow the installation instructions (drag Sublime Text 3 to your Applications folder).

4. Open the Sublime Text 3 application. 

### Add Package Control

SublimeText has its own very popular package manager called Package Control. We'll use it to add extra features to Sublime Text, including a web development shortcut package called Emmet and a JavaScript syntax helper jshint.

1. Follow <a href="https://packagecontrol.io/installation" target="_new">Package Control's  "simple installation" instructions</a> to add Package manager to your Sublime Text. When you paste the large block of text, make sure you:
   -  use the Sublime Text 3 version, and 
   -  enter the text into the bottom rectangle of the Sublime Text console.

2. We access Package Control through the Sublime Text command palette. Open the palette by pressing `cmd+shift+p` from within Sublime Text. Type `Package Control`  in the command palette to see the list of things Package Control can do.


### Add Packages

1. Let's install our first package, Emmet.  Select `Package Control: Install Package` to bring up the list of available packages. 

2. Select `Emmet` from the list, and Package Control will install it for you!  (Start typing "Emmet" in the search bar to narrow down the list.)

The other package we plan to add, jshint, requires Node.js.  We'll get to it in the next set of instructions, linked at the bottom of this file.

### Access Sublime from the Terminal

Sublime Text 3 includes a program that launches Sublime from the Terminal.  We'll use the `ln` command to link that program to a simple `subl` command. 

1. To run a program from the Terminal, it needs to be available on your $PATH. The next step assumes `/usr/local/bin` is in your $PATH, so let's check that.  Run the following command from the Terminal to see your current $PATH:
    
    ```
    echo $PATH
    ```

1. Run the following command in your Terminal to set up the link:
    ```
    ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
    ```

2. Type `subl . ` in the Terminal, and Sublime Text 3 should open!

### Configure git to use Sublime

When you forget to enter a commit message in the Terminal, git opens a text editor and reminds you to add a commit message.

1. Run the following command in the Terminal to configure git to open Sublime Text instead of the default text editor:
    
    ```
    git config --global core.editor "subl"
    ```

## Node, Express & Mongo

1. Install Node.js, a platform for back end web development with the JavaScript programming language. 
2. Install JSHint and its Sublime Text packages to get realtime JavaScript syntax hints.
3. Install MongoDB, the database we'll use with our Node.js and Express stack. 

## Node.js

1. Install Node.js with homebrew by running the following command in the Terminal.

  ```
  brew install node
  ```

2. Run the Terminal command `which node` to check that Node.js was installed. The Terminal command `node` changes your Terminal into a Javascript REPL ("Read Evaluate Print Loop"), like the right hand side of <a href="http://repl.it" target="_new">repl.it</a>.  Type `control+C` twice to quite out of the REPL and return to the normal Terminal commands.

3. Run the Terminal command `which npm` to check that npm is installed. The Node Package Manager, used through various `npm` commands, is a lot like Homebrew, except we'll use it for Node.js-specific tools instead of for general Mac tools. NPM packages are often called "node modules."

### Nodemon

Nodemon (short for "node monitor") will make our node.js workflow more efficient. 

Install nodemon globally with the following command:
  
  ```
  sudo npm install -g nodemon
  ```


### JSHint for Sublime Text
It's time to install another Sublime Text package!

1. Select `Package Control: Install Package` to bring up the list of available packages.  Select `SublimeLinter` from the list, and Package Control will install it for you.

2. Repeat the step above to install the packages "SublimeLinter-jshint".

3. Follow the <a href="https://github.com/SublimeLinter/SublimeLinter-jshint" target="_new">SublimeLinter-jshint install instructions</a> to set up jshint on your laptop. You've just installed Node.js and npm, so you won't need to repeat that step.


## MongoDB

MonogDB is a popular noSQL database.  We'll use it to store data with our Node.js and Express stack. 

1. Use Homebrew to update all of our brew packages.

  ```bash
  brew update
  ```
2. Run `brew install` for **MongoDB**

  ```bash
  brew install mongodb
  ```

3. Then we'll need a directory for **MongoDB** to save data.

  ```bash
  sudo mkdir -p /data/db
  ```

4. Finally we'll want to make sure we have permission to read and write to this directory.

  ```bash
  sudo chown -R $USER /data/db
  ```

5. Run two commands to check whether the install worked. You should see a file path after each command.

  ```bash
  $ which mongod
  $ which mongo
  ```
