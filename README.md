# small

This project is for using vagrant and virtualbox to manage the environment for 
the Software Carpentry Training course.

##  TODO

in the same directory where the small directory is install create a directory 
name scripts 

-----------------------

## Basic Vagrant Commands
virtual >vagrant --help
Usage: vagrant [options] <command> [<args>]

    -v, --version                    Print the version and exit.
    -h, --help                       Print this help.

### Selected commands:
```
     destroy         stops and deletes all traces of the vagrant machine
     halt            stops the vagrant machine
     help            shows the help for a subcommand
     init            initializes a new Vagrant environment by creating a Vagrantfile
     ssh             connects to machine via SSH
     up              starts and provisions the vagrant environment
     version         prints current and latest Vagrant version
```
For help on any individual command run `vagrant COMMAND -h`

Additional subcommands are available, but are either more advanced
or not commonly used. To see all subcommands, run the command
`vagrant list-commands`.


