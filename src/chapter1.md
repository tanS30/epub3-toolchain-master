# Developing Simple Applications

Python is one of the most widely used dynamic programming languages. It supports a rich set of packages, GUI libraries, and web frameworks that enable you to build efficient cross-platform applications. It is an ideal language for rapid application development. Such fast-paced development often comes with its own baggage that could bring down the overall quality, performance, and extensibility of the code.
This course will show you ways to handle such situations and help you develop better Python applications. The key concepts will be explained with the help of command line applications, which will be progressively improved in subsequent chapters.

This chapter will be an introductory one. It will serve as a refresher to Python programming. That being said, it is expected you have some knowledge of Python language, as well as object-oriented programming (OOP) concepts.

Here is how this chapter is organized:

* We will start with installation prerequisites and setup a proper environment
for Python development.
* To set the tone right for the rest of the book, the next section will be a brief
introduction to the high fantasy theme of the book.
* What follows next is our first program. It is a simple text-based fantasy game,
presented as a Python script.
* We will add some complexity to this game and develop an incremental
version of the game using simple functions.
* Moving ahead, we will add more features to the game and redesign the code
by applying OOP concepts.

Review the code in the `ch01_ex03.py file`. In the next few chapters, you will learn techniques to progressively improve this code.


## Installation Prerequisites
Let's make sure that we have installed the prerequisites. Here is a table that
summarizes the basic tools we need for this chapter and beyond; more verbose
installation instructions follow in the next section:

![](assets/Python3.5.PNG)

## Installation of Python 3.5
For Linux or Mac users, Python is probably already installed on your system. If not, you can install it using the package manager of your operating system. Windows OS users can install Python 3.5 by downloading the Python installer from the official Python website:

![Installing Python 3.5](assets/Image1_01_01.png)

## Python install location
Let's briefly talk about the path where Python is installed, and how to make sure Python is available as a command in your terminal window. Of course, things will widely vary, depending on where you install it and which Python distribution you
choose.

The official Python documentation page has comprehensive information on setting up the Python environment on different platforms. Here is a link, in case you need further help beyond what we have covered: https://docs.python.org/3/using/index.html.


## Unix-like operating systems
On a Unix-like operating system such as Linux, the default location is typically `/usr/bin/python or /usr/local/bin/python`.

If you used your operating system's package manager to install Python, the command python or python3 should be available in the terminal window. If it isn't, you need to update the PATH system environment variable to include the directory path to the Python executable. For example, if you have aBash shell, add the following to the `.bashrc file` in your user home directory:

`export PATH=$PATH:/usr/bin/`

Specify the actual path to your Python installation in place of `/usr/bin`.


## Windows OS

On Windows OS, the default Python installation path is typically the following directory: `C:\Users\name\AppData\Local\Programs\Python\Python35-32\python.exe`. Replace name with your Windows username. Depending on your
installer and system, the Python directory can also be Python35-64. As mentioned earlier, at the time of installation, you should select the option Add Python 3.5 to `PATH` to make sure python or python.exe are automatically recognized as
commands. Alternatively, you can rerun the installer with just this option checked.

## Verifying Python installation
Open a terminal window (or Command Prompt on Windows OS) and type the following command to verify the Python version. This command will work if Python is installed and is available as a command in the terminal window. Otherwise,
specify the full path to the Python executable. For instance, on Linux you can specify it as `/usr/bin/python`, if Python is installed in `/usr/bin`:

```
$ python -V
```
Note that the `$` sign in the previous command line belongs to the terminal window and is not part of the command itself! Put another way, the actual command is just python `-V`. The `$` or `%` sign in the terminal window is a prompt for a normal user on Linux. For a root (admin) user, the sign is `#`. Likewise, on Windows OS, the corresponding symbol is `>`.
You will type the actual command after this symbol. The following is just a sample output, if we run the preceding command:

```
[user@hostname ~]$ python -V
Python 3.5.1 :: Anaconda 4.0.0 (64-bit)
```
## Installing pip
The pip is a software package manager that makes it trivial to install Python packages from the offi cial third party software repository,PyPI. The pip is already installed for Python-2 version 2.7.9 or higher and Python-3 version 3.4 or higher.
If you are using a different Python version, check out https://pip.pypa.io/en/stable/installing for the installation instructions.
On Linux OS, the default location for the pip is same as that of the Python executable. For example, if you have /usr/bin/python, then pip should be available as `/usr/bin/pip`. On Windows OS, the default pip.exe is typically the following:
```
C:\Users\name\AppData\Local\Programs\Python\Python35-32\Scripts\pip.exe.
```
As mentioned earlier, replace name with your Windows username. Depending on your installer and the system, the Python directory can also be Python35-64.

## Installing IPython
This is an optional installation. IPython is an enhanced version of the Python interpreter. If it is not already bundled in your Python distribution, you can install it with:
```
$ pip install ipython
```
After the installation, just type ipython in the terminal to start the IPython interactive shell. Here is a screenshot of the IPython shell using the Anaconda Python 3.5 distribution:

![Installing IPython](assets/Image_01_02.png)

## Choosing an IDE
Using an IDE for development is a matter of personal preference. Simply put, an
IDE is a tool intended to accelerate application development. It enables developers
to write effi cient code quickly by integrating the most common tools they need.

<video id="video1" controls="controls">
  <source type="video/mp4" src="assets/Video_01.mp4"/>
</video>

## The theme of this course
Have you read high fantasy novels, such as The Lord of the Rings or The Hobbit by J. R. R. Tolkien? Or watched the films based on these novels? Well, here is a high fantasy, "Tolkienesque" themed book on Python application development.

This course takes you to an imaginary world where you will develop a text game based on the aforementioned theme. Yes, you can continue being a developer even in this imaginary world! During the course of the book, you will be accompanied by
many fictional characters. While you learn different aspects of Python development, these characters will talk to you, ask questions, request new features, and even fight with the enemy.
It should be noted that this book is not about developing game applications. It uses a simple text-based game just as a medium to learn various development aspects.

Let's meet the imaginary characters who will accompany you in various chapters:

![Meet the characters](assets/output_dDbbiG.gif)

*Sir Foo*:
A human knight who is portrayed as a grand knight guarding the southern plains. He is our main character and will be talking to us throughout the book.

*Orc Rider*:
An Orc is a human-like imaginary creature. Here, it is portrayed as an enemy soldier. The Orc is seen riding a wild boar-like creature.

*Elf Rider*:
An Elf is a supernatural mythical being. The Elf is mounted on an elvish horse. He is portrayed as a friendly.

*Fairy*:
An intelligent fairy with an inherent capability for magic.

*Dwarf*:
A Dwarf is a small human-like mythical being. He is portrayed as "The Great Dwarf" of the Foo mountains.
He asks lots of questions.
