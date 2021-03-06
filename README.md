# MicroTXT 💻

A tiny [textboard style](https://en.wikipedia.org/wiki/Textboard) software written in PHP, no database required.

It is meant to be simple to use, host, and develop.

## Features

* ✅ Only PHP 5.x+ required (No database server, only sqlite3!)
* ✅ Hidden/unlisted threads (start your thread title with .)
* ✅ MOTDs
* ✅ Less than 300kb uncompressed
* ✅ Markdown for parent posts
* ✅ No JavaScript required (JavaScript is used minimally but only to increase usability)

## Installing

MicroTXT is only tested in a Linux environment, however, it should work on Windows/Unix with little to no modification.

Simply download and place the files in your PHP 5+ enabled website directory, and edit php/settings.php to your liking. You should probably also change rules.txt and faq.txt too.

**PHP 5.X support will be dropped when PHP 5.6 reaches EOL, I suggest migrating to PHP 7.x before then.**

**YOU NEED PHP MBSTRING AND SQLITE3 LIBRARIES INSTALLED**

**You also need the GD PHP library installed on your PHP instance if you want to use the included captcha**

## Configuring

Just edit php/settings.php

To disable the captcha just change $captcha to false, or to make the captcha appear every time, change $postsBeforeCaptcha to 0.

## Warnings

This is new, there may be some issues with it.

Don't rely on it for huge communities, it doesn't scale for very high traffic projects (it's not meant to).

Change the salt in settings.php, otherwise tripcodes may be easier to brute force.

**Prior to version 1.2, salts were not being applied to tripcodes (due to a bug), resulting in potentially easy to brute force tripcodes when bad passwords were used**

**Prior to version 1.6, links in parent posts could potentially cause XSS with javascript: and data uris (reported by @arinerron)**

Tripcodes are 'secure enough' if you set a good salt and good passwords are used for the codes, but in general they should not be considered to be 100% proof of a poster's identity.

## Demo

You can use the demo board [on my website](https://www.chaoswebs.net/mt/).

## Contributing

I will accept pull requests if they fix bugs or improve the software in a way I think fits the goals of the project.

Try to follow the coding style of existing code, and comment any non-simple code.

### Bug Reports

Well structured & polite bug reports are appreciated. Please try to include the following information in any bug reports:

* PHP version
* Web server version
* Operating system version
* MicroTXT Version (specified in settings.php)
* What you have tried so far
* Screenshots are helpful, but not necessarily required.

## Development Roadmap & Planned features

* Better post & reply formatting
* Admin panel for setup, configuration, and moderation
* Easy to use installation script (For Linux)
* Perhaps a Docker container if there is demand
* Code refactoring

## Contacting me

You can get in touch with me [here](https://chaoswebs.net/contact)

## Donate 💲

If you want to support development, a dollar or two would be appreciated. If you donate, get in touch with me so I know what work you would like me to do for the project.

Bitcoin/BCH: 1Hek4bVGsxSFA1QpTXryMZcP88agGMKfAU

[Or, donate another way](https://chaoswebs.net/)
