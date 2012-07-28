# freck
## A friendly command-line interface for Freckle

freck is a command-line tool that makes it easy to enter data to [Freckle](http://letsfreckle.com).

The first time you run it, freck will prompt you for your account details and current project.
Then logging your time is as easy as:

    freck 2h

or

    freck 6h "debugging the frobnicator"

You can add tags as well:

    freck "2 days" refactoring spifflication "refactoring the spifflication engine"

As usual with Freckle, an argument that is two words or fewer is treated
as a tag, and longer arguments are treated as description.

If you work on more than one project concurrently, you can specify the
project name using the `-p` option. You can even create new projects
right from the command line using `-c`, which tells freck to create
the named project if it doesn’t already exist.

If your project has standard tags that need to be applied to most of your tasks,
you can specify a default set of tags that will be included unless overridden
with the `-t` option.

## Installation

freck has no library dependencies. It requires only Python 2.6 or later,
present by default on current Linux and Mac distributions. Installation is
as simple as downloading the script to your bin directory and marking it
executable, e.g.

    curl -Lo ~/bin/freck https://github.com/robinhouston/freckle-command/raw/master/freck
    chmod 755 ~/bin/freck

## Usage

    Options:
      -h, --help            show this help message and exit
      -l, --list-projects   list all available projects
      -t TAGS, --tags=TAGS  additional tags, overriding the default if any
      -d DATE, --date=DATE  the date this task was done, if not today: yyyy-mm-dd
      -u USER, --user=USER  email address of user to record time for, if not you
      -p PROJECT, --project=PROJECT
                            the name of the project. If you have specified a
                            default you can miss this out
      -c, --create          create the project if it does not exist
      -v, --verbose         print detailed logging messages
      -s, --silent          print no informational messages
