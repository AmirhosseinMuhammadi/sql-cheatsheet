# SQL Cheatsheet
SQL (Structured Query Language) is the standard language to interact with relational databases. This cheatsheet is based on courses available on [Sololearn](https://www.sololearn.com/) and AI guidelines.

## Table of Contents
- [Relational Database Management System (RDBMS)](#relational-database-management-system-(rdbms))
 - [SQLite](#sqlite)
 - [MySQL (MariaDB)](#mysql-(mariadb))
 - [PostgreSQL](#postgresql)
## Relational Database Management System (RDBMS)
A Relational Database Management System (RDBMS) is a software system used to store, manage, and retrieve structured data. It organizes data into tables consisting of rows and columns, allowing relationships to be defined and enforced between them. RDBMSs use SQL (Structured Query Language) as the standard language for querying and updating data. The scope of an RDBMS includes data modeling, indexing, transaction management, and enforcing integrity rules to ensure accuracy and consistency. RDBMS solutions such as SQLite, MySQL, and PostgreSQL provide reliable and efficient data handling for applications ranging from small local programs to large-scale distributed systems.

### SQLite
**Prerequisites**
- No server required (SQLite is an embedded database).
- Works on Linux, macOS, and Windows.
- Only needs the **SQLite CLI** (optional if your language/framework already includes it e.g. Python).

**Installation & Setup**
- Linux (Debian/Ubuntu):
```bash
sudo apt update
sudo apt install sqlite3
```

- Arch/Manjaro
```bash
sudo pacman -S sqlite
```

- macOS
 ```bash
brew install sqlite
```

- Windows

Available on https://sqlite.org/download.html.

### MySQL (MariaDB)
**Prerequisites**
- Requires running database server.
- Recommended usage for medium/large web apps.
- GUI tools (optional): DBeaver, HeidiSQL, MySQL Workbench.

**Installation & Setup**
- Linux (Debian/Ubuntu):
```bash
sudo apt update
sudo apt install mysql-server
sudo systemctl enable mysql
sudo systemctl start mysql
```

- Arch/Manjaro
```bash
sudo pacman -S mariadb
sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
sudo systemctl enable mariadb
sudo systemctl start mariadb
```

- macOS
 ```bash
brew install mysql
brew services start mysql
```

- Windows

The installer is available on https://dev.mysql.com/downloads/installer/.

### PostgreSQL
**Prerequisites**
- Requires running database server.
- Strong ACID guarantees, recommended for serious backend systems.
- GUI tools (optional): pgAdmin, DBeaver, TablePlus.

**Installation & Setup**
- Linux (Debian/Ubuntu):
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl enable postgresql
sudo systemctl start postgresql
```

- Arch/Manjaro
```bash
sudo pacman -S postgresql
sudo -iu postgres initdb --locale=$LANG -D '/var/lib/postgres/data'
sudo systemctl enable postgresql
sudo systemctl start postgresql
```

- macOS
 ```bash
brew install postgresql
brew services start postgresql
```

- Windows

The installer (includes pgAdmin) is available on https://www.postgresql.org/download/windows/.
