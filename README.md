# SubdomainsScanner

knock
Knock Subdomain Scan
 Introduction

Knock allows you to scan subdomains, Transfer Zone discovery, Wildcard testing with internal or external wordlist.
This program is self contained, doesn’t need to be installed in any particular location. All it needs is a recent version of Python 2.x
Only for use the Zone Transfer option (-zt) you must install the module dnspython, otherwise you can do without. If the name server allows zone transfers to occur, all the DNS names and IP addresses hosted by the name server will be returned in human-readable ASCII text.
Usage

    $ python knock.py <option> <url>

Rapid Scan

    Scanning with internal wordlist:

    $ python knock.py <url>

    Scanning with external wordlist:

    $ python knock.py <url> <wordlist>

Options

    -zt Zone Transfer discovery:

    $ python knock.py -zt <url>

    -dns Dns resolver:

    $ python knock.py -dns <url>

    -wc Wildcard testing:

    $ python knock.py -wc <url>

    -bw Wildcard bypass:

    $ python knock.py -bw <stringexclude> <url>

Executable on Linux

    Download knock tar.gz archive and extract file knock.py

    From shell command:

    $ sudo cp knock.py /usr/local/bin/knock
     $ sudo chmod a+x /usr/local/bin/knock

    Now you can use knock as shown in the examples.

Executable on Windows

    Download knock zip archive, extract folder and use file knock.exe

    Required: Python 2.x and Dnspython

Examples

    Scanning with internal wordlist

    $ ./knock domain.com

    Scanning with external wordlist

    $ ./knock domain.com wordlist.txt

    Zone Transfer discovery (-zt)

    $ ./knock -zt domain.com

    Dns resolver (-dns)

    $ ./knock -dns domain.com

    Wildcard testing (-wc)

    $ ./knock -wc domain.com

    Wildcard bypass with internal wordlist (-wc)

    $ ./knock -bw stringexclude domain.com

    Wildcard bypass with external wordlist (-wc)

    $ ./knock -bw stringexclude domain.com wordlist.txt

Sample stdout to file

    This will cause the ouput of a knock to be written to a text file

    $ ./knock domain.com > output.txt

