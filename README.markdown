PDF Movement Tray
=================

This is a web based version of the [Movement Tray][m] tool. The aim of this 
project is to provide an easy to use web interface to the command line tool.

The web interface will look like this:

![Web Interface](http://i.imgur.com/irRaWFr.png)

The command line tool generates a printable movement tray for war games which
use 20 or 25mm square bases. A good example of such system is
Warhammer Fantasy Battles which uses 20mm and 25mm bases for most of
the infantry models.

The tray is generated as a PDF file that will look approximately like this:

![Sample Output](http://i.imgur.com/xiF3QVp.jpg)

Configuration
-------------

The back end dependencies are managed via [Bundler][b]. To install all the
required gems do:

    bundle install

The front end dependencies are managed via [Bower][t]. To install do:

    bower install

If you are deploying on a host with Passenger you restart the application by
doing:

    touch tmp/restart.txt
    
Please note that the [Prawn][p] gem requires Ruby 1.9.3 or better. If you are still on 1.8.7 and are unable to upgrade (for example, if you are using shared hosting) you will need to downgrade Prawn down to version 0.8.4. To do so edit the `Gemfile` and change the prawn entry to:

    gem 'prawn', '~> 0.8.4'
    
You can leave all the other dependencies the same. The 0.8.4 version of the gem has all the necessary functionality to run this tool and has been confirmed to be fairly stable in production.

Dependencies
------------

This tool depends on the following gems:

* [Sinatra][s] - web framework
* [Bundler][b] - back end dependency management
* [Bower][t] - front end dependency management
* [Prawn][p] - for PDF generation

Following front end libraries are used:

* [Bootstrap][a] - basic layout
* [jQuery][j] - javascript framework
* [Zero Clipboard][z] - automated copy/paste actions
* [jQuery-ZeroClipboard][c] - jQuery wrapper for Zero Clipboard

[m]: https://github.com/maciakl/MovementTray
[p]: http://prawn.majesticseacreature.com
[s]: http://www.sinatrarb.com/
[b]: http://bundler.io/
[t]: http://bower.io/

[a]: http://getbootstrap.com/
[j]: http://jquery.com/
[z]: http://zeroclipboard.org/
[c]: https://github.com/balsamiq/jquery-zeroclipboard
