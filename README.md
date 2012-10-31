#derpoker

derpoker is the nuclear option for that poke war you've been in on facebook. Just configure your facebook
credentials and where you want to log your poking activity to and let the script do the rest.


## Running the script

### Requirements
To run the auto poking script you're going to need the selenium python module and selenium java server. Instructions on how to obtain them
can be found on the [pypi website][selenium]

If you'd like to also run your own version of the webserver which displays results, you'll have to install and setup all of the django goodness.
Everything that you need to run the webserver on Heroku with S3 as your static file storage is included in the repo. If people are interested in
detailed instructions on how to set this up, I'd be more than happy specify them. For right now I've really gotta get back to homework.

### Setup
In order to run derpoker you need to create a file called `facebook.py` in the same directory as `autopoker.py`. You can easily do this by just
copying `facebook-skel.py` to `facebook.py` and entering in your appropriate information. For more info on what the `SQL_CONNECT_STRING` can look
like, go checkout [SQL Alchemy's documentation on how their engines work][sqlal].


### Running
To run you need to do two things. First run the selenium server with:

    java -jar selenium-server-standalone-2.25.0.jar

Leave that running and then start the autopoker script:

  python autopokes.py

That's it!


## Who Are You?

derpoker is the result of the idle hands of [Kurtis Nusbaum][kln].
I really like computers and programming.

## License
derpoker is licensed under the [GPLv2][gpl].


[kln]:https://github.com/klnusbaum/
[gpl]:https://github.com/klnusbaum/derpoker/blob/master/LICENSE
[selenium]:http://pypi.python.org/pypi/selenium
[sqlal]:http://docs.sqlalchemy.org/en/latest/core/engines.html
