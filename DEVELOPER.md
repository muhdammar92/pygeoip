# Bootstrap manual for developers
_Dependencies: tox, nose, epydoc_

### Testing

For testing we are using tox virtualenv-based Python version testing
and nose as test framwork.

Tox will create virtualenvs for all Python version pygeoip supports
and installs the current working tree using the setup.py install script.
Running the tests requires a couple of sample databases found on the
link below.

Maxmind sample databases for testing can be downloaded here:
http://www.defunct.cc/maxmind-geoip-samples.tar.gz (58 MB)

Extract the tarball in the tests directory and run `tox` from the root directory.

This requires a machine with Python 2.5 - 3.3 installed and all dependencies mention in the header.

### Documentation

The documentation can be re-generated by running epydoc from repository root.

    epydoc --config=epydoc.ini --no-private

For converting Markdown to reStructuredText used by PyPi we use pandoc.
[Read pandoc's install instructions](http://johnmacfarlane.net/pandoc/installing.html).

### TL;DR

There's a shell script doing all this for you.

    ./build.sh
