# freck
## a friendly command-line interface for Freckle

freck is a command-line tool that makes it easy to enter data to [Freckle](http://letsfreckle.com).

The first time you run it, freck will prompt you for your account details and current project.
Then logging your time is as easy as:

    freck 2h

to record a two-hour task. You can add tags and/or a description, too:

    freck -t "tag1, tag2, This is a description" "2 days"

If you work on more than one project concurrently, you can specify the
project name using the `-p` option. You can even create new projects
right from the command line using `-c`, which tells freck to create
the named project if it doesn’t already exist.

freck has no library dependencies. It requires only Python 2.6 or later,
present by default on current Linux and Mac distributions. Installation is
as simple as downloading the script to your bin directory and marking it
executable, e.g.

    curl -o ~/bin/freck https://github.com/robinhouston/freckle-command/raw/master/freck
    chmod 755 ~/bin/freck

## Usage

    Usage: freck [options] time_spent

    Options:
      -h, --help            show this help message and exit
      -l, --list-projects   list all available projects
      -t TAGS, --tags=TAGS  a list of tags and/or a description, comma-separated
      -p PROJECT, --project=PROJECT
                            the name of the project. If you have specified a
                            default you can miss this out
      -d DATE, --date=DATE  the date to record this task against, yyyy-mm-dd
      -c, --create          create the project if it does not exist
      -v, --verbose         print detailed logging messages
      -s, --silent          print no informational messages
