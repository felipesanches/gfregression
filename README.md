# Google Fonts Regression Tester

Compare local font families against each other, or if a Google Fonts family, again the lastest release hosted on fonts.google.com

Web version can be found [here](http://35.238.63.0/)

# ![GF Regression Screenshot](screenshot.png)

**Warning: Error handling and better tests are needed. This webapp should not be treated as a God. It should be used in conjunction with good judgement.**

*"Measure twice, cut once" - English Proverb*

## Installation

### Run from Docker

Create a new docker machine:

    docker-machine create gf-regression

Run the machine:

    docker-machine start gf-regression

Log into machine:

    docker-machine env gf-regression
    # Copy and paste the returned text in your shell.

Build and run the container using docker-compose. Make sure you are in the project's root directory.

    python2 -m virtualenv venv
    # Activate the virtualenv
    docker-compose up

Find out where the app is listening:

    docker-machine ls
    # Copy the _bare_ IP address from the "URL" column and paste it into your browser, no port and no tcp://!

### Run app directly

To run GF Regression locally, you'll need a [Google Fonts API key](https://developers.google.com/fonts/).
This must be stored in a json file located at `/app/secrets.json` with the following structure:

    {
        "GF_API_KEY": "YOUR-GF-API-KEY"
    }
