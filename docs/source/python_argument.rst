
Argument
========

https://docs.python.org/3/library/argparse.html

https://docs.python.org/zh-cn/3/howto/argparse.html

https://docs.python.org/zh-cn/3/library/argparse.html#module-argparse



.. code:: python

   import argparse

   parser = argparse.ArgumentParser(description='Process some integers.')
   parser.add_argument('integers', metavar='N', type=int, nargs='+',
                       help='an integer for the accumulator')
   parser.add_argument('--sum', dest='accumulate', action='store_const',
                       const=sum, default=max,
                       help='sum the integers (default: find the max)')

   args = parser.parse_args()
   print(args.accumulate(args.integers))



.. code::

   ArgumentParser(
     prog=None,                               #The name of the program (default: sys.argv[0])
     usage=None,                              #The string describing the program usage (default: generated from arguments added to parser)
     description=None,                        #Text to display before the argument help (default: none)
     epilog=None,                             #Text to display after the argument help (default: none)
     parents=[],                              #A list of ArgumentParser objects whose arguments should also be included
     formatter_class=argparse.HelpFormatter,  # A class for customizing the help output
     prefix_chars='-',                        #The set of characters that prefix optional arguments (default: ‘-‘)
     fromfile_prefix_chars=None,              #The set of characters that prefix files from which additional arguments should be read (default: None)
     argument_default=None,                   #The global default value for arguments (default: None)
     conflict_handler='error',                # The strategy for resolving conflicting optionals (usually unnecessary)
     add_help=True,                           #Add a -h/--help option to the parser (default: True)
     allow_abbrev=True                        #Allows long options to be abbreviated if the abbreviation is unambiguous. (default: True)
   )

   ArgumentParser.add_argument(
     name or flags...  # Either a name or a list of option strings, e.g. foo or -f, --foo.
     [, action]        # The basic type of action to be taken when this argument is encountered at the command line.
                       #  'store' - This just stores the argument’s value. This is the default action.
                       #  'store_const' -  This stores the value specified by the const keyword argument.
                       #  'store_true' and 'store_false' - These are special cases of 'store_const' used for storing the values True and False respectively.
                       #  'append' - This stores a list, and appends each argument value to the list.
                       #  'append_const' - This stores a list, and appends the value specified by the const keyword argument to the list.
                       #  'count' - This counts the number of times a keyword argument occurs.
                       #  'help' - This prints a complete help message for all the options in the current parser and then exits.
                       #  'version' - This expects a version= keyword argument in the add_argument() call, and prints version information
                       #  'extend' - This stores a list, and extends each argument value to the list.
     [, nargs]         # The number of command-line arguments that should be consumed.
                       #  N (an integer). N arguments from the command line will be gathered together into a list.
                       #  '?'. One argument will be consumed from the command line if possible, and produced as a single item.
                       #  '*'. All command-line arguments present are gathered into a list.
                       #  '+'. Just like '*', all command-line args present are gathered into a list.
                       #  argparse.REMAINDER. All the remaining command-line arguments are gathered into a list.
     [, const]         # A constant value required by some action and nargs selections.
     [, default]       # The value produced if the argument is absent from the command line.
     [, type]          # The type to which the command-line argument should be converted.
     [, choices]       # A container of the allowable values for the argument.
     [, required]      # Whether or not the command-line option may be omitted (optionals only).
     [, help]          # A brief description of what the argument does.
     [, metavar]       # A name for the argument in usage messages.
     [, dest]          # The name of the attribute to be added to the object returned by parse_args().
     )


