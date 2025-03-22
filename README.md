# Tanzania Regions, Districts, Wards, and Villages Database

This repository contains an updated database structure for regions, districts, wards, and villages in Tanzania. The database was created to provide a comprehensive and accurate data source for use in various applications.

## Database Structure

The database consists of the following tables:

1. **Regions**: Contains the regions of Tanzania.
2. **Districts**: Contains the districts, each linked to a specific region using the `region_id`.
3. **Wards**: Contains the wards, each linked to a specific district using the `district_id`.
4. **Villages**: Contains the villages, each linked to a specific ward using the `ward_id`.

### Table Relationships:
- The **Regions** table has a primary key `id`.
- The **Districts** table contains a foreign key `region_id` which references `id` from the Regions table.
- The **Wards** table contains foreign key `district_id` referencing the `id` of Districts, respectively.
- The **Villages** table contains foreign key `ward_id`.

## Installation

To use the database in your project:

1. Clone this repository:
    ```bash
    git clone https://github.com/issahakimu/tanzania-regions-districts-wards-villages.git
    ```

2. Import the SQL file into your MySQL database:
    - Log in to your MySQL database.
    - Create a new database (or use an existing one):
      ```sql
      CREATE DATABASE tanzania_db;
      ```
    - Select the database:
      ```sql
      USE tanzania_db;
      ```
    - Import the SQL file:
      ```sql
      SOURCE /path/to/database/Tanzania.sql;
      ```

3. The tables and relationships will be created in your database.

## Usage

You can query the database to fetch regions, districts, wards, and villages. Here are some examples of queries you can run:

- To get all regions:
  ```sql
  SELECT * FROM regions;

4. Update the database configuration in your application to connect to this database.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to fork this repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries, feel free to contact:
- Email: issahakimuakida365@gmail.com
- GitHub: https://github.com/issahakimu