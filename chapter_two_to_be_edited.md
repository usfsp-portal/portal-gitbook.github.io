E
rrata
The following seems to be needed any time we import a SQL dump (at least the way we've been doing it) since that entails dropping and recreating the database:

DROP USER 'ossp'@'localhost'; CREATE USER 'ossp'@'localhost' IDENTIFIED BY '****************'; GRANT ALL PRIVILEGES ON ossp.* TO 'ossp'@'localhost'; FLUSH PRIVILEGES;
