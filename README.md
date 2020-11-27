# gitsql tool 1.0

Backup database MySQL from command line (LINUX)

### How it work
Very simple, by run script ./gitsql.sh you get access to commands. Backup-s are stored in the same directory gitsql/db

![screen](screen.png)

### Install

#### Clone repo

```bash
git clone git@github.com:damian-pm/gitsql.git
```
(Optional)
You can move repo to /home dir and create alias
For example in .bash_aliases

```bash
alias gitsql='~/gitsql-tool/gitsql.sh' 
```

### Configuration

Edit file gitsql.sh, rename USER_LOGIN with login to database and USER_PASS with password to database
```bash
USER_LOGIN="damian"
USER_PASS="damian"
PORT=3306
HOST=localhost
```

### Available commands

```bash
gitsql list [get list of backups]
gitsql list db [get list of databases]

gitsql import db_sub_name [if db_name not specifed, db_sub_name will be db_name ] db_name [optional] 
gitsql export db_name db_sub_name [optional] 

gitsql zip db_name [zip file to db_zip/ if exists will replace]
gitsql unzip db_name [unzip file to db/ if exist will replace]
```
