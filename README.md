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
* Rating: ratings from [IMDB](https://www.imdb.com), [Rotten Tomatoes](https://www.rottentomatoes.com/) and [Metacritic](http://www.metacritic.com/movie)
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

* List all episodes in Game of Thrones season 6
```bash
~ $ omdb game of thrones -s 6
Find 10 result(s)

+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
|        Title         |      Time       |      Genre      |   Length   |        Rating        |        Actor         |
+======================+=================+=================+============+======================+======================+
| The Red Woman        | 24 Apr 2016     | Adventure,      | 50 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 8.4 (22230)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Emilia Clarke        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| Home                 | 01 May 2016     | Adventure,      | 54 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 9.5 (28139)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Kit Harington        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| Oathbreaker          | 08 May 2016     | Adventure,      | 52 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 8.7 (17050)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Emilia Clarke        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| Book of the Stranger | 15 May 2016     | Adventure,      | 59 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 9.2 (18525)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Emilia Clarke        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| The Door             | 22 May 2016     | Adventure,      | 54 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Emilia Clarke, Kit   |
|                      |                 |                 |            | IMDB: 9.7 (38565)    | Harington, Aidan     |
|                      |                 |                 |            |                      | Gillen               |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| Blood of My Blood    | 29 May 2016     | Adventure,      | 52 min     | Rated: TV-MA         | Nikolaj Coster-      |
|                      |                 | Drama, Fantasy  |            |                      | Waldau, Lena Headey, |
|                      |                 |                 |            | IMDB: 8.4 (16978)    | Emilia Clarke,       |
|                      |                 |                 |            |                      | Natalie Dormer       |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| The Broken Man       | 05 Jun 2016     | Adventure,      | 56 min     | Rated: TV-MA         | Peter Dinklage, Kit  |
|                      |                 | Drama, Fantasy  |            |                      | Harington, Liam      |
|                      |                 |                 |            | IMDB: 8.6 (15623)    | Cunningham, Nikolaj  |
|                      |                 |                 |            |                      | Coster-Waldau        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| No One               | 12 Jun 2016     | Adventure,      | 59 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 8.2 (18250)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Emilia Clarke        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| Battle of the        | 19 Jun 2016     | Adventure,      | 60 min     | Rated: TV-MA         | Peter Dinklage, Kit  |
| Bastards             |                 | Drama, Fantasy  |            |                      | Harington, Emilia    |
|                      |                 |                 |            | IMDB: 9.9 (131896)   | Clarke, Liam         |
|                      |                 |                 |            |                      | Cunningham           |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
| The Winds of Winter  | 26 Jun 2016     | Adventure,      | 69 min     | Rated: TV-MA         | Peter Dinklage,      |
|                      |                 | Drama, Fantasy  |            |                      | Nikolaj Coster-      |
|                      |                 |                 |            | IMDB: 9.9 (87754)    | Waldau, Lena Headey, |
|                      |                 |                 |            |                      | Kit Harington        |
+----------------------+-----------------+-----------------+------------+----------------------+----------------------+
```
