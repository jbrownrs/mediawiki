# Mediawiki Docker-compose configuration
Docker-compose configuration which launches a ​Mediawiki​ instance using MariaDB as a database.
When launched, the Mediawiki instance is available at http://localhost:8000/.

## Getting Started
Ensure that the host system has directories mediawiki_data and db_data in the current directory.

To launch the instance run:
`docker-compose -f docker-compose.yml up`

In your browser navigate to http://localhost:8000/.

Log in using the database username and password provided in the LocalSettings.php then edit away!

## Restoring the database
To restore the database run:
`cat initdb.sql | docker exec -i CONTAINER /usr/bin/mysql -u Admin --password=supersecret my_wiki`
where CONTAINER is your container ID - this can be checked using `docker ps`.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details
