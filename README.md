# Introduction to Tandem

Tandem is a node-baseds scripting language used for performing simulations. It's useful for writing simulations, hardware descriptions, and other programs that are best expressed as state-machines that involve transitions between functions.

# Dependencies

* Java 1.5 or greater
* [ANTLR3](http://www.antlr.org) (if you want to compile the grammar)
* [Apache Ant](http://ant.apache.org/)
* [JUnit](http://www.junit.org/) (for running the compiler tests)
* [Ruby 1.9.2+](http://www.ruby-lang.org/en/) (you can also use JRuby)
* [Bash](http://www.gnu.org/software/bash/)
* Awk
* sed

Except for Java, Ant, Bash, and Awk, all the other dependencies will be downloaded for you if you use Ant, thanks to Apache Ivy. If you are using a modern Linux distribution or are using Mac OS X, you will have Bash and awk already.

Support for Windows is limited to Ant. Note that you will need to compile all imported files yourself if you are on Windows. On Unix systems, the tandem compiler will take care of this for you.


To install ANTLR manually, first download the [JAR file](http://www.antlr.org/download.html). Make sure that you add the path to the JAR file to your classpath.

# Compilation and Installation using Ant

The easiest way to use Tandem is to use Ant, a tool similar to `make`.

	$ git clone git://github.com/vrdabomb5717/Tandem.git
	$ cd Tandem

Now, create the build, dist, lib, and grammar directories, download the dependencies, and compile the grammar:

	$ ant init
	$ ant grammar

At this point, the file will complain if it cannot find ANTLR in your classpath.

Compile the rest of the files, and try running the tests:

	$ ant compile
	$ ant test

Running `ant test` will create the needed directories, compile the grammar, compile the parser and lexer, and test the files using JUnit. It may be easier to just use that.

For more specific tests, `ant gunit_test` will run the grammar tests and `ant parse_test` will run the parser tests that require JUnit.

to traverse the tree, run `ant walk` with a filename provided as an argument.

For example, try traversing the tree with expression.td:

	$ ant walk -Dfile=test/expression/expression.td


# Cleaning up and Uninstallation

To clean up without deleting your entire Tandem installation, run `ant clean`. To clean up the dependencies that you have downloaded as well, run `ant clean-ivy`.

If you would like to remove the entire Tandem installation, just delete the entire Tandem directory.


# Compilation and Installation without using Ant

To compile the grammar file, assuming that ANTLR is on your classpath, run:

	$ java org.antlr.Tool TanG.g
	$ javac TandemTree.java
	$ java TandemTree $INPUTFILE

More instructions will come at a later date!

# Known Bugs

* You cannot currently chain method calls when using imported Ruby code.
* If you do not use the main Tandem compiler, you will need to compile all imported Tandem files, recursively, before you compile the specified .td file.
