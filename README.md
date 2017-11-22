# ClausIE -- Clause-Based Open Information Extraction
It is a mavenized version of [ClauseIE](https://www.mpi-inf.mpg.de/departments/databases-and-information-systems/software/clausie/) project in [Max Planck Institute](https://www.mpi-inf.mpg.de/home/) (configuration and resource files as well as some of the codes structure are modified).

ClausIE is an open information extractor, it identifies and extracts relations and their arguments in natural language text. ClausIE first detects "useful" pieces of information expressed in a sentence, and then represents this information in terms of one or more extractions. The representation of these extractions can be flexibly customized to the underlying application (e.g., binary or n-ary propositions).

Here is the online test provided by Max Planck Institute: **[ClausIE online demo!](https://gate.d5.mpi-inf.mpg.de/ClausIEGate/ClausIEGate)**.

ClausIE codes download: [[link]](http://resources.mpi-inf.mpg.de/d5/clausie/clausie-0-0-1.zip).

ClausIE tutorials: [[link]](http://resources.mpi-inf.mpg.de/d5/clausie/tutorial_.html).

## Requirements
- [Java 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).
- JOpt Simple (A Java library for parsing command line options, `version>=4.4`), its maven snippet: [[link]](https://mvnrepository.com/artifact/net.sf.jopt-simple/jopt-simple).
- [Stanford Parser](https://stanfordnlp.github.io/CoreNLP/) (It is a program that works out the grammatical structure of sentences, `version==2.0.4`), its maven snippet: [[link]](https://mvnrepository.com/artifact/edu.stanford.nlp/stanford-parser/2.0.4), since ClausIE uses the pre-trained parser model of Stanford Parser, please also add the following model dependency:
```XML
<dependency>
    <groupId>edu.stanford.nlp</groupId>
    <artifactId>stanford-parser</artifactId>
    <version>${stanford-parser.version}</version>
    <classifier>models</classifier>
</dependency>
```

## Usage
A pre-built ClausIE `jar` file is located at [`target/ClausIE.jar`](/target/), it includes the `JOpt` and `Stanford Parser` and its model already, which can be add into your project and used directly. (Use IntelliJ to build `jar` file please refer: [[link]](https://stackoverflow.com/questions/12508180/how-do-you-mavenize-a-project-using-intellij))

Or, you can clone this source and follow the article [Maven in 5 Minutes](http://maven.apache.org/guides/getting-started/maven-in-five-minutes.html) to make some changes and mavenize it to use in your own project. To add it as a maven dependency:
```XML
<dependencies>
    ...
    <dependency>
        <groupId>de.mpii.clausie</groupId>
        <artifactId>clausIE</artifactId>
        <version>1.0-SNAPSHOT</version>
    </dependency>
    ...
</dependencies>
```
