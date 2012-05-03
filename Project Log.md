# Project Log

## 4/26/12

Started on the tree grammar for the parser. Need to rewrite 3 or so rules to do the transformations for magnitude comparisons, equality testing, and the pipeline. Started work on the code generator, where a Ruby file is created within the Java code.

## 4/25/12

Worked on unit tests. Added target for TreeWalker, fixed whitespace bugs in grammar, prevented users from adding lists, sets, or hashes to the pipeline. Worked on understanding how to write the Tree grammar, and improved on visualizing the nodes that were created in the AST.

## 4/19/12

Got unit tests automation working, so running `ant test` will run the entire compilation process. Added assignments, literals, and corrected associativites on the grammar. Also fixed comments in the grammar.

## 4/18/12

Created a test file that can parse a file and report whether it parses correctly or not so we can run unit tests. Converted arithmetic, logical, and bitwise expressions with correct precedences.

## 4/8/12

Debated about whether we should have true division or integer division. Made project structure and added them to Github. Got git up and running on everyone's computer, and taught everybody the basic commands to push, pull, commit, and checkout code. Started writing the ANTLR grammar, and discovered ANTLRWorks, an IDE to work on the ANTLR file, display the DFA for the grammar, and check the grammar.

## 3/29/12

Went over the comments that Prof. Aho and Shuai sent us about the LRM, realizing that some of their complaints were just located elsewhere in the LRM. Debated about the tool we should use to write the grammar, and finally settled on ANTLR. Realized that we would need to rewrite the grammar as LL(\*), so started working on the transformations needded from LR(1) to LL(\*).

## 3/20/12

Continued working on the tutorial and finished the grammar. Added the grammar to the LRM, and asked others for sample programs to add to the tutorial. Started talking about what to write the grammar in. Realized that yacc's support for outputting to Java is experimental at best, so looked at ANTLR, JCup, JFlex. Also realized that the dynamic typing we would need prevent us from writing Java code. Evaluated Python, Ruby, and Groovy code, and decided to choose Ruby as our code target.

## 3/19/12

Added keywords like while and for. Fixed the pipeline to allow for multiple pipelines and literals in the pipeline. Added operator, associativity, and operation meaning table. These include arithmetic, boolean, logical, and bitwise operators.

## 3/1/12

Began working on the grammar. Decided that nodes can only call imported nodes, and that you cannot create nodes within other nodes. Nodes are static, and are compiled down to Java classes, and any code in the main section of the code is the main node, located in the main function of the Java class. Created import, node, main body, whitespace, and basic pipeline production in the grammar.

## 2/26/12

Met to start working on the syntactic features of the language. Decided that we should have pipelines, like in Unix, to have function calls. Planned out the aspects of the grammar that we would need, expressions we wanted, and conditionals and loops that we might need.

## 2/15/12

Discussed features of the language. Decided that the language should be used for hardware, network state programming, game theory programs, neural networks, networking programs, and simulations. The programming language is platform independent, nodal, threaded, dynamic, compiled, functional, modular, and massively parallel. Assigned parts of the white paper to the others, and asked them to be done by 2/20 so we could have some time to review the language. Decided to call the language Tandem.

## 2/2/12

Discussed ideas on what sort of language to create. Talked about functional language ideas, languages for parallel programming, languages to do finite state machines, languages like Python and Ruby (general-purpose languages), and other ideas. Decided to create a finite state machine language.