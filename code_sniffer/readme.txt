This is the WordPress Coding Standards extension of phpcs.
We have set this up to run in a docker container

Setup:
IN a terminal from this directory run:
setup
source ~/.bashrc

Use:
Navigate to the directory containing your source code.

To run the code sniffer report run:
cdccs

To run the code beautifier and fixer run:
cdccbf


The cdccs and cdcbf will run the code sniffer and code beautifier and fixer on the current working directory
using the WordPress standard

You can get crazy with how you run this by calling the docker container directly.  This way you can pass any arguments you want, like if you only want to test a single file, or if you want to change the standard.
Check out the cdccs and cdcbf scripts to see how to call the container directly.  To run on a single file
replace the . with the file name.  You can also pass any arguments after that to configure phpcs.

Documentation:
https://github.com/squizlabs/PHP_CodeSniffer/wiki
https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards

