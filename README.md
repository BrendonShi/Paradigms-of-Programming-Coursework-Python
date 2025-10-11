# 🌳 Family Tree Relationship Finder

This project is a Python application designed to build a family tree from a CSV file and determine the relationships between any two individuals in the tree. It uses an object-oriented approach to model people and their connections, providing a clean and extensible way to explore genealogical data.

---

## ✨ Features

-   **Object-Oriented Design**: Utilises classes for `Person`, `Relationship`, and `FamilyTree` to create a structured and logical model of the family data.
-   **CSV Data Import**: Automatically builds the family tree by reading data from a `family_tree.csv` file.
-   **Relationship Calculation**: Can find and display the relationship between any two people in the tree (e.g., "Grandmother", "Son", "Cousin").
-   **Extensible Structure**: The class-based design makes it easy to add more complex relationships or functionalities.
-   **Unit Tested**: Includes a suite of unit tests (`unittest_family.py`) to ensure the core logic is working correctly.

---

## 📂 Project Structure

The project is broken down into several key files, each with a specific responsibility.

| File                  | Description                                                                                                      |
| :-------------------- | :--------------------------------------------------------------------------------------------------------------- |
| `main.py`             | The main entry point for the application. It loads the data, builds the tree, and finds the relationship.          |
| `FamilyTree.py`       | Contains the `FamilyTree` class, which manages all the people and the logic for finding relationships.           |
| `person.py`           | Defines the `Person` class, which stores information about an individual (ID, name, gender, parents).            |
| `relationship.py`     | Defines the `Relationship` class, which represents the connection between two people.                            |
| `list.py`             | A helper module used by the `FamilyTree` class to manage lists of people.                                        |
| `family_tree.csv`     | The data file containing the family information. New members can be added here.                                  |
| `unittest_family.py`  | Contains unit tests to verify the functionality of the `FamilyTree` and `Person` classes.                        |

---

## ⚙️ How to Use

To get started with the application, follow these steps.

### 1. Prepare the Data

The family data is stored in `family_tree.csv`. The file must contain the following columns:

-   `id`: A unique number for each person.
-   `name`: The person's first name.
-   `gender`: The person's gender (`Male` or `Female`).
-   `parent1_id`: The ID of the first parent.
-   `parent2_id`: The ID of the second parent.

Here is an example of the format:
```csv
id,name,gender,parent1_id,parent2_id
1,John,Male,,
2,Mary,Female,,
3,Peter,Male,1,2
4,Susan,Female,1,2
```
---
### 2. Run the Application
To find the relationship between two people, you will need to modify the main.py file to set the names of the two individuals you want to compare.

```python
# In main.py, change "Peter" and "Susan" to the names you want to find
person1_name = "Peter"
person2_name = "Susan"
```
Then, run the main script from your terminal:
```bash
python main.py
```
The application will print the relationship between the two specified people.

### 3. Testing
The project includes a set of unit tests to ensure everything is working as expected. You can run these tests using Python's built-in unittest module:

```bash
python -m unittest unittest_family.py
```
