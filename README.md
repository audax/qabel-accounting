# Qabel Accounting Server

[![Build Status](https://travis-ci.org/Qabel/qabel-accounting.svg?branch=master)](https://travis-ci.org/Qabel/qabel-accounting)

## Requirements
Python 3.4 or 3.5

## Installation

Create a virtualenv for the project

	virtualenv -p python3.4 ../venv
	source ../venv/bin/activate
	pip install -r requirements.txt

Run the migrations

	./manage.py migrate

## Running tests

The tests are run by the py.test framework. You can choose which browser you want to use for the functional tests.

Phantomjs: (recommended)

	py.test --splinter-webdriver phantomjs

Firefox:

	py.test --splinter-webdriver firefox

## Production setup

See the [django documentation](https://docs.djangoproject.com/en/1.8/howto/deployment/)

In your django settings you have to set an API_SECRET that should be known only by the
qabel-block server.
