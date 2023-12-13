# DDL exercise3
Creating Tables with Null and Not Null Constraints:
Create a table named Planets with the following columns:

planet_id (integer)
planet_name (varchar, maximum length 50, not null)
diameter (decimal)
distance_from_sun (decimal, not null)
Ensure that planet_name column does not allow NULL values, while distance_from_sun can have NULL values.

```SQL
CREATE TABLE planets(planet_id INT, planet_name VARCHAR(50) NOT NULL, diameter DECIMAL, distance_from_sun DECIMAL);

DESCRIBE planets;
+-------------------+---------------+------+-----+---------+-------+
| Field             | Type          | Null | Key | Default | Extra |
+-------------------+---------------+------+-----+---------+-------+
| planet_id         | int           | YES  |     | NULL    |       |
| planet_name       | varchar(50)   | NO   |     | NULL    |       |
| diameter          | decimal(10,0) | YES  |     | NULL    |       |
| distance_from_sun | decimal(10,0) | YES  |     | NULL    |       |
+-------------------+---------------+------+-----+---------+-------+
```

Altering Tables with Not Null Constraints:
Alter the Planets table to modify the diameter column to not allow NULL values.

```SQL
ALTER TABLE planets MODIFY diameter DECIMAL NOT NULL;

+-------------------+---------------+------+-----+---------+-------+
| Field             | Type          | Null | Key | Default | Extra |
+-------------------+---------------+------+-----+---------+-------+
| planet_id         | int           | YES  |     | NULL    |       |
| planet_name       | varchar(50)   | NO   |     | NULL    |       |
| diameter          | decimal(10,0) | NO   |     | NULL    |       |
| distance_from_sun | decimal(10,0) | YES  |     | NULL    |       |
+-------------------+---------------+------+-----+---------+-------+
```

Dropping Tables:
Create a new table named Galaxies with the following columns:

galaxy_id (integer)
galaxy_name (varchar, maximum length 50, not null)
description (text)
number_of_stars (integer)
Then, drop the Galaxies table
```SQL

CREATE TABLE galaxies(galaxy_id INT, galaxy_name VARCHAR(50) NOT NULL, description TEXT, number_of_stars INT);
DESCRIBE galaxies;

+-----------------+-------------+------+-----+---------+-------+
| Field           | Type        | Null | Key | Default | Extra |
+-----------------+-------------+------+-----+---------+-------+
| galaxy_id       | int         | YES  |     | NULL    |       |
| galaxy_name     | varchar(50) | NO   |     | NULL    |       |
| description     | text        | YES  |     | NULL    |       |
| number_of_stars | int         | YES  |     | NULL    |       |
+-----------------+-------------+------+-----+---------+-------+

DROP TABLE galaxies;

SHOW TABLES;
+----------------+
| Tables_in_mydb |
+----------------+
| books          |
| diningspots    |
| events         |
| movies         |
| planets        |
| users          |
| users2         |
+----------------+
```