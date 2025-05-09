## Here is a sample project to migrate sqlite3 database file into MySQL Database.

*Here I used [`sqlite3-to-mysql`](https://github.com/techouse/sqlite3-to-mysql.git ) tool from Github. Which help me save my time and effort. It is basically running the command and it's done.
Here I will guid you how I did a sample migration from sqlite3 db file into MySQL database*.

**Step 1:** Here I assume you already have `sqllite3` and `MySQL` install in your machine.

**Step 2:** Goto this link [`sqlite3-to-mysql`](https://github.com/techouse/sqlite3-to-mysql.git ) and goto `README` file. There are 3 steps to install the tool in your machine. 
- [1]. install python package, 
- [2]. Install Docker image, 
- [3]. Install Homebrew package. 

*Note:* Since I have MacOS I used the brew option to intall the tool in my machine.

**Step 3:** Run this Command
```
brew tap techouse/sqlite3-to-mysql
brew install sqlite3-to-mysql
sqlite3mysql --help
```

**Step 4:** Create a Database in mysql
login to MySQL and run 
```
mysql -u root -p
Create database <database_name>
```
**Step 5:** Goto terminal and run the command
```
sqlite3mysql -f chinook.db -d chinookdb -u root -p
```

*Note:* Here I have downloaded the chinookdb file from internet specifically for this project so I used this file you can use any file you like.

**Step 6:** You can try sqlite3mysql --help for more option.

**Step 7:** Congratulation!!! You are all set.