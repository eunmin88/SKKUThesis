# SKKUThesis
# Prerequisites 
* unzip data_old.zip
* unzip data_new.zip
* sudo apt-get install python3 python3-pip
* pip3 install -r requirements.txt
# Running Program
* python3 run.py -d ./data_old -q question_# -s 100 -f -m -b
# Command Line arguments
* -d flag specifies the path of data directory (data_old for previous, data_new for my updated)
* -q flag specifies the question (folder) name within data directory (Must write number 1~5 in place of #)
* -s flag specifies the sampling rate. With -s 0 option, only the instructor provided reference program is used to repair buggy student programs. -s 100 option indicates that 100% of correct student programs (along with the instructor provided reference program) are used.
* -f flag applies the refactoring rules on all correct programs in an offline phase. 
* -m flag enables structure mutation phase, where the control flow structure of buggy program is mutated to match the closest refactored correct program. This phase occurs only if no refactored program with an exact control flow match is found, after the refactoring phase (-o or -f flag).
* -b flag enables the block repair phase, where blockwise repair of buggy programs is performed by synthesizing a patch based on blockwise input-output specification of aligned (refactored) correct program
