# signatures
Tool that generates an ltrace config file for a dynamic library.

    ./signatures.pl <libname.so>

# genprototypes
Tool that generates function prototypes for all functions of a C source file.

    ./genprototypes.pl [options] <source-file>

    Options:
      --max-columns=<N>, -c Max number of columns per line
      --run-tests, -t       Run unit tests only
# gencpp
Tool that receives a C++ header file and generates its .cpp skeleton file. **Work in progress**.

    ./gencpp.pl6 -h=<C++ header>

# genunittest
Tool that receives a C source file and generates a unit test skeleton file with all external functions already mocked (using fff.h), except for system calls. Too dependent on GCC version.

    ./genunittest.pl [options] -- <.c file>
    
    Options:
      --exclude=<pattern> Excluded files
             -x <pattern>
      
      --test-func=<funcs> List of functions to which test cases should be created
               -f <funcs>
      
           --path=<paths> Extra dirs to search for included headers
               -p <paths>
               
              --overwrite Force overwriting of the output file if it exists
                       -o
                       
              --int-tests Try and generate also a integration tests module
                       -i
                       
            --interactive Activates interactive mode
                       -n
                       
# imported_symbols
Tool that lists all imported symbols of a binary file, specifying what dynamic libraries each symbol comes from.

    ./imported_symbols.pl <binary>

# ip-range
Tool that generates custom IPv4 ranges.

    ./ip-range.pl <first-IPv4-address> <count>
    
    e.g: ./ip-range.pl 192.168.1.1 3
        192.168.1.1
        192.168.1.2
        192.168.1.3

# listsources
Tool that receives a binary file (with debug symbols) and lists all source files that were used to generate it.

    ./listsources.pl <binary-file>

# mockheader
Tool that receives a C header file and create fff.h mocks for all functions.

    ./mockheader.pl [options] <header-file>
    
    Options:
      --out-file=<filename> Output file. Omit to print to stdout
              -o <filename>
     --mock-suffix=<suffix> Preferred suffix to add to mocked functions
                -s <suffix>

# print_struct
Tool to generate C code to print the contents of a struct. Depends on the https://github.com/rubiot/perl6-c-parser. Partial implemention only. **Work in progress**.

# perf-rubio
Script to automate network throughput tests. Depends on other scripts not available here.

    ./perf-rubio.pl <test duration> <IMIX genome> <#ports>
