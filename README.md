# PLAY BY PLAY AND BOX SCORE SCRAPING LIBRARY


## Requirements


This library was created on a Mac, so the setup instructions are geared toward a *nix environment (sorry Windows users)

* Python 2.5 or greater
* MySQL
* MySQLdb - Python's API to the MySQL database

TODO: Add postgres, sqlite support

## Instructions


* Clone the repository to your local machine (change your_folder_path to whatever folder you want to put the repo)

```
cd your_folder_path
git clone git@github.com:kpascual/nbascrape.git
```

* Add this new directory to your PYTHONPATH in ~/.bash_profile

```
PYTHONPATH="/your_folder_path/nbascrape:$PYTHONPATH"
export PYTHONPATH
```

* Go to the libscrape/config
* Copy constants_example.py to constants.py, and edit rows 3-8 in constants.py with the path containing this repo.

```
cd libscrape/config
cp constants_example.py constants.py
```

* Copy db_example.py to db.py, and enter your MySQL database credentials

```
cp db_example.py db.py
```

```
vi db.py

  4 dbconn_prod = {
  5     'user': 'username_here',
  6     'passwd': 'password_here',
  7     'db': 'database_name_here'
  8 }
```

To actually do scraping, run the master.py file within the libscrape directory, and enter the date (YYYY-MM-DD) of the games that you want to scrape.

```
cd your_path_here/libscrape
python master.py 2012-10-30
```

