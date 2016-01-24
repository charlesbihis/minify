# Minify

A simple Java utility for minifying JSON code in your Java application.

## Overview

This library is built for use with Java applications for the purpose of minifying JSON code.  This work is an adaptation of JSMin.java written by John Reilly (www.inconspicuous.org) which is itself a translation of jsmin.c written by Douglas Crockford (www.crockford.com).

## Reference

Minify has a simple utility method for producing minified JSON:

	/**
	 * Minifies the input JSON string.
	 * 
	 * Takes the input JSON string and deletes the characters which are insignificant to JavaScipt.  Comments will
	 * be removed, tabs will be replaced with spaces, carriage returns will be replaced with line feeds, and most
	 * spaces and line feeds will be removed.  The result will be returned.
	 * 
	 * @param json The JSON string for which to minify
	 * @return A minified, yet identically functional, version of the input JSON string
	 */ 
	public String minify(String json)

Note: Minify also has a second utility method for producing minified JSON from a stream of input, if you'd like to work directly with streams.

## Usage

To use the library, simply instantiate an instance of the Minify class and invoke one of the minify() utility methods:

	String minifiedJson = new Minify().minify(unminifiedJson);

## Author

* Created by Charles Bihis
* Website: [www.whoischarles.com](http://www.whoischarles.com)
* E-mail: [charles@whoischarles.com](mailto:charles@whoischarles.com)
* Twitter: [@charlesbihis](http://www.twitter.com/charlesbihis)

## Relevant

* Adapted from [JSMin.java](http://www.unl.edu/ucomm/templatedependents/JSMin.java) written by John Reilly (www.inconspicuous.org)
* Adapted from [jsmin.c](http://www.crockford.com/javascript/jsmin.c) written by Douglas Crockford (www.crockford.com).

## License

Permission is hereby granted to use this Java version under the same conditions as the original jsmin.c on which all of these derivatives are based.  See the header on Minify.java for more.