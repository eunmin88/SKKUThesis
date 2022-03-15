# SKKUThesis
#Command Line arguments
##-d flag specifies the path of data directory
##-q flag specifies the question (folder) name within data directory
##-s flag specifies the sampling rate. With -s 0 option, only the instructor provided reference program is used to repair buggy student programs. -s 100 option indicates that 100% of correct student programs (along with the instructor provided reference program) are used.
-o flag enables online refactoring phase to generate new semantically equivalent correct programs.
-f flag applies the refactoring rules on all correct programs in an offline phase. During the online phase, the closest aligned refactored program is chosen for repair. Note that our implementation does not support online and offline (-o and -f flags) simultaneously.
-m flag enables structure mutation phase, where the control flow structure of buggy program is mutated to match the closest refactored correct program. This phase occurs only if no refactored program with an exact control flow match is found, after the refactoring phase (-o or -f flag).
-b flag enables the block repair phase, where blockwise repair of buggy programs is performed by synthesizing a patch based on blockwise input-output specification of aligned (refactored) correct program
