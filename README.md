# DDL exercise3
Creating Tables with Null and Not Null Constraints:
Create a table named Planets with the following columns:

planet_id (integer)
planet_name (varchar, maximum length 50, not null)
diameter (decimal)
distance_from_sun (decimal, not null)
Ensure that planet_name column does not allow NULL values, while distance_from_sun can have NULL values.

Altering Tables with Not Null Constraints:
Alter the Planets table to modify the diameter column to not allow NULL values.

Dropping Tables:
Create a new table named Galaxies with the following columns:

galaxy_id (integer)
galaxy_name (varchar, maximum length 50, not null)
description (text)
number_of_stars (integer)
Then, drop the Galaxies table
