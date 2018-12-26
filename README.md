# README #

Hawkbeans is a small (~6K LOC), MIT-licensed JVM written in C. It does **not** meet the Java specification (not even
close), but includes enough functionality for students to become familiar with
concepts important to the JVM, viz. byte code interpretation, exceptions,
class loading, resolution of symbolic references, exceptions, stack frames,
and garbage collection.

Below are a list of features **not** supported in this JVM:

* Full exception support: only the basics.
* Reflection
* Floating point math is hardly tested
* User-defined class loaders
* Extremely limited JNI
* No JIT compilation
* Wide word support is limited
* No actual protection is implemented (i.e. private/public etc.)

Hawkbeans uses a simple buddy allocator with power of 2 free lists
for heap management. This code was taken from several other
OS code bases.

Hawkbeans was developed referencing Oracle's [Java Virtual Machine
Specification](https://docs.oracle.com/javase/specs/jvms/se8/html/index.html).


### Setup ###

You'll need a JDK 1.8 environment installed to build programs to run
with Hawkbeans (i.e. using javac). 

### Building ###

To build the JVM, simply run `make`. To build the Java libs (required for
building test programs) run `make jlibs`. 

### Running ###
Hawkbeans can be run as follows:

`$> ./hawkbeans SomeClass.class`


