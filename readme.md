GMail Atom Feed Command
=======================

Very basic script to retrieve a Gmail atom feed ; for example get unread 
message count. Originally created to get unread count in Byobu.

## Usage
    gmail-feed [-h] [-u, --username USERNAME] [-p, --password PASSWORD]
                      [-l, --label LABEL] [-c, --count-only]

    optional arguments:
        -h, --help            show this help message and exit
        -u, --username USERNAME
                              your gmail login (prompted if not specified)
        -p, --password PASSWORD
                              your gmail password (prompted if not specified)
        -l, --label LABEL     gmail label to retrieve (default is `unread`)
        -c, --count-only      if specified, only outputs the number of entries in
                              the feed.

## How to use in byobu
Create a file `60_gmail` in `$HOME/.byobu/bin` which invokes 
`gmail-feed -u <user> -p <passwd> -c` to get the number of unread messages
(60 stands for "every 60 seconds").
