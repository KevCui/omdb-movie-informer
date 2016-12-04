---
Title: movie-informer
Description: look up movie/TV series information from OMDb
Author: KrazyCavin
Tags: CLI, python, script
created:  04 Dec 2016
---

movie-informer
==============
Show movie or TV series information, using API from [OMDb](http://www.omdbapi.com/)<br/>
:warning: The request is slow because OMDb is :snail:

### What kind of information this script will display?
* Title: movie/TV series title
* Time: release time (day, month and year)
* Genre
* Length: runtime
* Rating: rating scores from [IMDB](https://www.imdb.com), [Rotten Tomatoes](https://www.rottentomatoes.com/) and [Metacritic](http://www.metacritic.com/movie)
* Actors

### Requirement
* Python3
* texttable

### Install python package
* pip install texttable

### How to use
```
usage: omdb [-h] [-y [YEAR]] [-s [SEASON]] [-d] searchtext [searchtext ...]

positional arguments:
  searchtext            search text

optional arguments:
  -h, --help            show this help message and exit
  -y [YEAR], --year [YEAR]
                        year of release
  -s [SEASON], --season [SEASON]
                        season number
  -d, --debug           active debug log
```
:warning: With **-d**, a debug log file **omdb.log** will be created in repo directory.

### Example
* List new star wars movie
```bash
~ $ omdb route one -y 2016
Find 1 result(s)

+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
|        Title         |      Time       |      Genre      |   Length   |        Rating        |        Actors        |
+======================+=================+=================+============+======================+======================+
| Rogue One: A Star    | 16 Dec 2016     | Action,         | 133 min    |                      | Felicity Jones, Mads |
| Wars Story           |                 | Adventure, Sci- |            |                      | Mikkelsen, Ben       |
|                      |                 | Fi              |            |                      | Mendelsohn, Riz      |
|                      |                 |                 |            |                      | Ahmed                |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
```
