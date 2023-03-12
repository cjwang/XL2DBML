# XL2DBML
Document database schema in Excel. Convert it to DBML. 


+----------+-------------+----------+-------------+-------------+---------------+
| Table    | Field       | Data     | Primary     | Referential | Relationship  |
| Name     | Name        | Type     | Key         | Constrain   | Type          |
|          |             |          |             |             |               |
| users    | id          | int      | True        |             |               |
|          | username    | varchar  |             |             |               |
|          | email       | varchar  |             |             |               |
|          | password    | varchar  |             |             |               |
|          | created_at  | datetime |             |             |               |
|          | updated_at  | datetime |             |             |               |
| posts    | id          | int      | True        |             |               |
|          | user_id     | int      |             |  users.id   | many-to-1     |
|          | title       | varchar  |             |             |               |
|          | body        | text     |             |             |               |
|          | created_at  | datetime |             |             |               |
|          | updated_at  | datetime |             |             |               |
| comments | id          | int      | True        |             |               |
|          | post_id     | int      |             |             |               |
|          | user_id     | int      |             |             |               |
|          | body        | text     |             |             |               |
|          | created_at  | datetime |             |             |               |
|          | updated_at  | datetime |             |             |               |
+----------+-------------+----------+-------------+-------------+---------------+

Relationship Type. In this column, you can use different values to indicate different types of relationships, such as:
1-to-1
1-to-many
many-to-1
many-to-many

Run the Python code to parse the Excel file and generate the DBML.

