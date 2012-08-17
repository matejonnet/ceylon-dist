# Ceylon distribution

This is the Milestone 4 "Ratatouille" release of the Ceylon command line tools (version 
0.4). This is a pre-release version of the platform for review by the community.

Ceylon is a programming language for writing large programs in a team environment. 
The language is elegant, highly readable, extremely typesafe, and makes it easy to 
get things done. And it's easy to learn for programmers who are familiar with 
mainstream languages used in business computing. Ceylon has a full-featured 
Eclipse-based development environment, allowing developers to take best advantage 
of the powerful static type system. Programs written in Ceylon execute on any 
Java 7 compatible JVM or Node.js.

Read more about Ceylon at <http://ceylon-lang.org>.

## Distribution layout

- `bin`            - Unix/Windows commands
- `doc`            - Documentation about Ceylon including the spec in HTML and PDF format
- `lib`            - Required libraries for the Ceylon commands
- `repo`           - Required bootstrap Ceylon modules (language, tools)
- `runtime-repo`   - Required runtime Ceylon modules (module system)
- `samples`        - Sample Ceylon modules
- `LICENSE-ASL`    - The Ceylon ASL license
- `LICENSE-GPL-CP` - The Ceylon GPL/CP license
- `README.md`      - This file

The command line tools are located in the `bin` directory.

- `bin/ceylon`     - Run a Ceylon program on the Java VM
- `bin/ceylon-js`  - Run a Ceylon program on node.js (JavaScript)
- `bin/ceylonc`    - Compile a Ceylon program for the Java backend
- `bin/ceylonc-js` - Compile a Ceylon program for the JavaScript backend
- `bin/ceylond`    - Document a Ceylon program

The API documentation for the language module `ceylon.language` may be found here:

- `repo/ceylon/language/0.4/module-doc`

## Running the sample programs

To compile and run the samples, start from the distribution directory containing
this file.

### Sample module

To run the "hello world" program, type:

    cd samples/helloworld

For Java:

    ../../bin/ceylonc com.acme.helloworld
    ../../bin/ceylond -non-shared -source-code com.acme.helloworld
    ../../bin/ceylon com.acme.helloworld/1.0.0 John

For JavaScript:

    ../../bin/ceylonc-js com.acme.helloworld
    ../../bin/ceylon-js com.acme.helloworld/1.0.0

### Sample with no module

To run a program defined in the default module, type:

    cd samples/no-module

For Java:

    ../../bin/ceylonc default
    ../../bin/ceylond -non-shared -source-code default
    ../../bin/ceylon default

For JavaScript:

    ../../bin/ceylonc-js default
    ../../bin/ceylon-js default

### Sample module with Java interoperability

To run the "Java interop" program, type:

    cd samples/interop-java
    ../../bin/ceylonc com.acme.interop
    ../../bin/ceylond -non-shared -source-code com.acme.interop
    ../../bin/ceylon com.acme.interop/1.0.0 John

Note: this is only available for the Java backend.

## Tool usage

To see a list of command line options, type one of:

    ./bin/ceylonc -help
    ./bin/ceylonc-js -help
    ./bin/ceylond -help
    ./bin/ceylon -help
    ./bin/ceylon-js -help

## Ant tasks for Ceylon

We include support for Ceylon ant tasks which are documented on
at <http://ceylon-lang.org/documentation/1.0/reference/tool/ant/>.

To run the "hello world" program using ant, type:

    cd samples/helloworld
    ant

## Source code

Source code is available from GitHub:

<http://github.com/ceylon>

## Issues

Bugs and suggestions may be reported in GitHub's issue tracker.

## Systems where Ceylon is known to work

Since Ceylon is running on the JVM it should work on every platform that 
supports a Java 7 compatible JVM. However we have tested the following 
platforms to make sure it works:

### Linux

- Ubuntu "precise" 12.04 (64 bit) JDK 1.7.0_03 (IcedTea), 
- Fedora 17 (64 bit) JDK 1.7.0_03 (IcedTea)
- Fedora 16 (64 bit), JDK 1.7.0_b147 (IcedTea)

### Windows

- Windows 7 (64 bit) 1.7.0_05 (Oracle)
- Windows Server 2008 R2 SP1 JDK 1.7.0_04

### OSX

- OSX 10 Lion (10.7.3) JDK 1.7.0_05 (Oracle)

## License

The Ceylon distribution is and contains work released

- partly under the ASL v2.0 as provided in the `LICENSE-ASL` file that accompanied 
  this code, and
- partly under the GPL v2 + Classpath Exception as provided in the `LICENSE-GPL-CP`
  file that accompanied this code.

### License terms for 3rd Party Works

This software uses a number of other works, the license terms of which are 
documented in the `NOTICE` file that accompanied this code.

### Repository

The content of this code repository, [available here on GitHub][ceylon-dist], 
is released under the ASL v2.0 as provided in the `LICENSE-ASL` file that accompanied 
this code.

[ceylon-dist]: https://github.com/ceylon/ceylon-dist

By submitting a "pull request" or otherwise contributing to this repository, you
agree to license your contribution under the license mentioned above.

## Acknowledgement

We're deeply indebted to the community volunteers who contributed a substantial part
of the current Ceylon codebase, working often in their own spare time. The following 
people have contributed to this release:

Gavin King, Stéphane Épardaud, Tako Schotanus, Emmanuel Bernard, Tom Bentley, Aleš Justin, 
David Festal, Flavio Oliveri, Max Rydahl Andersen, Mladen Turk, James Cobb, Tomáš Hradec, 
Michael Brackx, Ross Tate, Ivo Kasiuk, Enrique Zamudio, Julien Ponge, Julien Viet,
Pete Muir, Nicolas Leroux, Brett Cannon, Geoffrey De Smet, Guillaume Lours, Gunnar Morling,
Jeff Parsons, Jesse Sightler, Oleg Kulikov, Raimund Klein, Sergej Koščejev, Chris Marshall,
Simon Thum, Maia Kozheva, Shelby.
