# Tournament Results
Udacity Full Stack Web Developer Nanodegree (2016)
Project 4


##Files
* README.md — This file with introduction and instructions
* tournament.py -- implementation of a Swiss-system tournament
* tournament.sql -- table definitions for the tournament project.
* tournament_test.py -- Test cases for tournament.py

##Instruction to run

Start up vagrant and ssh into the database

```bash
vagrant $ vagrant up
vagrant $ vagrant ssh
```
Create tournament database & quit vagrant

```bash
vagrant@vagrant-ubuntu-trusty-32:~$ psql

psql (9.3.15)
Type "help" for help.

vagrant=> CREATE DATABASE tournament;
CREATE DATABASE
vagrant=> \q
```

Navigate to 'tournament' and load SQL

```bash
vagrant@vagrant-ubuntu-trusty-32:~$ cd /vagrant/tournament
vagrant@vagrant-ubuntu-trusty-32:/vagrant/tournament$ psql tournament < tournament.sql
```

run test

```bash
vagrant@vagrant-ubuntu-trusty-32:/vagrant/tournament$ python tournament_test.py
1. Old matches can be deleted.
2. Player records can be deleted.
3. After deleting, countPlayers() returns zero.
4. After registering a player, countPlayers() returns 1.
5. Players can be registered and deleted.
6. Newly registered players appear in the standings with no matches.
7. After a match, players have updated standings.
8. After one match, players with one win are paired.
Success!  All tests pass!
```
