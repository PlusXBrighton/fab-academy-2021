# Setting up mkdocs

https://www.mkdocs.org

Requires Python 3, and Macs by default come with Python 2.7, so this needs to be upgraded (but perhaps in a way that keeps 2.7 available for use by older packages)

https://docs.python-guide.org/starting/install3/osx/

Assuming you have Homebrew installed ...
> brew install python

Says it's already installed

```
Warning: python@3.9 3.9.1_6 is already installed and up-to-date
To reinstall 3.9.1_6, run 'brew reinstall python@3.9'
```

How to force it to be used...

# Set up a Python environment

https://opensource.com/article/19/5/python-3-default-mac

Install pyenv
> brew install pyenv


Use pyenv to install Python 3
> pyenv install 3.7.3

Nope didnt work

## Use Homebrew

Same page


> brew info python

Returns: python@3.9: stable 3.9.1 (bottled)

Add alias to my zshrc file

> echo "alias python=/usr/local/bin/python3.7" >> ~/.zshrc

Or just add this line into the file directly

And check the path, using `brew info python`. Actually mine is diffeent:

```
Python has been installed as
  /usr/local/bin/python3
```

So I need to edit that line.

Reload zsh profile: `source ~/.zshrc`

Check version again:
```
python --version                            ✔   6:44pm    26.01.2021 
Python 3.9.1
```

# Install mkdocs

sudo pip3 install mkdocs

Note:
* use sudo to override permissions errors
* use pip3 to force python 3

# Set up a sample site

https://www.mkdocs.org/#getting-started

> cd /Users/andrew/Documents/Git
> mkdocs new mkdocs-test

Or create an mkdocs site in the current directory:

> mkdocs new .

> cd mkdocs-test
> mkdocs serve

Cmd-period to stop the server and issue new commands

# Publish HTML to Github

https://squidfunk.github.io/mkdocs-material/publishing-your-site/

If you prefer to deploy your project documentation manually, you can just invoke the following command from the directory containing the mkdocs.yml file:

'mkdocs gh-deploy --force'
