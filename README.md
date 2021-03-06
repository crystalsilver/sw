# sw - suckless webframework

sw is a minimal and sane web framework.

## Installation

Run:

`make && make install PREFIX=/usr/local`

## Configuration

Copy sw.conf and style.css to your working directory, and edit them to fit your needs.

## Static web generation

Run from your working directory:

`sw /path/to/site`

Where 'site' is the folder where your website is located.
The static version of the website is created under 'site.static'.

## Automatic generation+upload

The whole process can be automatized if you create a Makefile like this in your working directory:

```make
all:
	sw /path/to/site
	rsync -avz site.static/ foo.org:/path/to/wwwroot/
clean:
	rm -rf site.static
```

## Author

* Nibble \<develsec.org\>

## Contributors

* pancake \<nopcode.org\>
* Andrew Antle
