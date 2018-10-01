Elasticsearch Analysis Kuromoji UniDic Neologd
=======================

## Overview

Elasticsearch Analysis Neologd Plugin provides Tokenizer/CharFilter/TokenFilter for Kuromoji with Neologd.

## Version

[Versions in Maven Repository](http://central.maven.org/maven2/org/codelibs/elasticsearch-analysis-kuromoji-neologd/)

### Issues/Questions

Please file an [issue](https://github.com/codelibs/elasticsearch-analysis-kuromoji-unidic-neologd/issues "issue").
(Japanese forum is [here](https://github.com/codelibs/codelibs-ja-forum "here").)

## Installation

    $ $ES_HOME/bin/elasticsearch-plugin install org.codelibs:elasticsearch-analysis-kuromoji-unidic-neologd:6.4.0

## References

### Analyzer, Tokenizer, TokenFilter, CharFilter

The plugin includes these analyzer and tokenizer, tokenfilter.

| name                                             | type        |
|:-------------------------------------------------|:-----------:|
| kuromoji\_unidic\_neologd\_iteration\_mark       | charfilter  |
| kuromoji\_unidic\_neologd                        | analyzer    |
| kuromoji\_unidic\_neologd\_tokenizer             | tokenizer   |
| kuromoji\_unidic\_neologd\_baseform              | tokenfilter |
| kuromoji\_unidic\_neologd\_part\_of\_speech      | tokenfilter |
| kuromoji\_unidic\_neologd\_readingform           | tokenfilter |
| kuromoji\_unidic\_neologd\_stemmer               | tokenfilter |

### Usage

See [Elasticsearch Kuromoji](https://github.com/elastic/elasticsearch-analysis-kuromoji "elasticsearch-analysis-kuromoji").

### Update Kuromoji Jar File

If you want to replace with the latest Lucene Neologd jar file, download it from http://maven.codelibs.org/org/codelibs/lucene-analyzers-kuromoji-unidic-neologd/ and then replace old file in $ES_HOME/plugins/analysis-kuromoji-unidic-neologd.

### What is NEologd

See [mecab-unidic-NEologd](https://github.com/neologd/mecab-unidic-neologd "mecab-unidic-NEologd").

## Use Lucene Kuromoji for Neologd

If you want to use Lucene Kuromoji for Neologd in your application other than elasticsearch, you can use lucene-analyzers-kuromoji-unidic-neologd jar file, not this plugin.
To use the jar file, put the following settings into your pom.xml.

    ...
    <repositories>
        <repository>
            <id>codelibs.org</id>
            <name>CodeLibs Repository</name>
            <url>http://maven.codelibs.org/</url>
        </repository>
    </repositories>
    ...
    <dependencies>
        <dependency>
            <groupId>org.codelibs</groupId>
            <artifactId>lucene-analyzers-kuromoji-unidic-neologd</artifactId>
            <version>6.4.0-20180927</version>
            <!-- http://maven.codelibs.org/org/codelibs/lucene-analyzers-kuromoji-unidic-neologd/ --->
        </dependency>
    ...

See [CodeLibs Maven Repository](http://maven.codelibs.org/org/codelibs/lucene-analyzers-kuromoji-unidic-neologd/).

