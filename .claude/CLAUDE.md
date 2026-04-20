# Claude Memory

## Project Overview

YAAML is a yaml parser implemented in Aalgola.

It includes the library and an executable command line program to work with yaaml files.

## Build System

The project uses the native Aalgola compile and build systems.

### Common Commands

```bash
# Compile program
aalgolac --compile-all --source-path sources/ --target target/classes/

# Run test (always compile before running test). Tests reference types from the
# main library, so both the compile step and aatest need the main classes on
# their modules path.
aalgolac --compile-all --source-path test/sources/ --target test/target/classes/ --modules-path target/classes/
aatest --modules test/target/classes/,target/classes/

# Run the yaaml program to parse yaml from stdin
aalgola --modules target/classes/ //github.com/robertbraeutigam/yaaml/Yaaml
```

## Note on Aalgola

The language itself is still under development. It can produce weird errors, unimplemented functions/methods
or even syntax errors where there is none.
