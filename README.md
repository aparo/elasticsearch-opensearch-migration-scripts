# Elasticsearch to Opensearch Migration Scripts

This is a collection of scripts that I use to migrate code/plugins from ElasticSearch to OpenSearch.

## Usage

There are two scripts that need to be copied in an user accessible path (ie. ~/bin/ )
- chcase: used to rename directories and files. I take it from [http://www.primaledge.ca/chcase.html](http://www.primaledge.ca/chcase.html). It`s a old script from 2005, but I'm affectionated to it. Use *chcase -e* for example of usage
- to-os: a bash script that do the job simplify the conversation from Elasticsearch to OpenSearch namespaces/names.

The renaming is not 100% effective, but it does automatically a lot of the effort required in migrating a plugin.

### Requirements
The prerequisites are perl and bash, that are generally installed in every Linux system and MacOS.

The perl regex module must be installed on the system otherwise you should have a similar error:
```
Can't locate Regexp/Common.pm in @INC (you may need to install the Regexp::Common module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at -e line 3.
BEGIN failed--compilation aborted at -e line 3.
```

On Ubuntu install it via: 
```
sudo apt-get install -y libregexp-common-perl
```

On Unix/Macos:
```
cpan Regexp::Common
```

### Future plan
Convert it in a Scala script via ammonite or a Python one.

## My Rationale

Due to license change of ElasticSearch to OSS license to a *dangerous* SSPL, it's not safe to manage my personal data assets in Elasticsearch anymore.
In my home lab I built different tools around Elasticsearch:
- link tech collector crawling system to retrieve latest new about my technology passions (ie Scala, ElasticSearch, OpenSearch)
- huge collection of datasets for NLP processing and AI developing
- a collection of Italian recipes for my wife/grandma
- the catalog of my book/manga collections
- all my indexed source code
- ...

IMHO, the rationals are not AWS vs Elastic, but [freedom](https://www.youtube.com/watch?v=f4Mc-NYPHaQ) vs lock-in. 
My position is more like [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman), but I am not a purist and I think the Apache 2 is a good licence. 

