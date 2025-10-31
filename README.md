# Degrees of Separation 🎬

A Python program that determines how many “degrees of separation” apart two actors are, based on shared movie appearances. Inspired by the **“Six Degrees of Kevin Bacon”** concept, this project finds the shortest path between any two actors using **breadth-first search (BFS)**.

---

## 🧠 Background

According to the Six Degrees of Kevin Bacon game, anyone in Hollywood can be connected to Kevin Bacon within six steps, where each step represents a movie shared by two actors.

This project generalizes that idea — you can input **any two actors**, and the program will compute the **shortest connection path** between them through their shared movies.

---

## 🗂️ Data

The repository includes two datasets:

* **`small/`** – a lightweight dataset for quick testing and experimentation
* **`large/`** – a full dataset for complete searches

Each dataset contains three CSV files:

* `people.csv` — contains actor IDs, names, and birth years
* `movies.csv` — contains movie IDs, titles, and release years
* `stars.csv` — links actors to the movies they starred in

For example, a line in `stars.csv` might indicate that **Kevin Bacon** starred in *A Few Good Men*.

---

## ⚙️ How It Works

The program builds three main data structures:

* `names` → maps lowercase actor names to their corresponding IDs
* `people` → maps each person’s ID to their details and list of movie IDs
* `movies` → maps each movie’s ID to its details and list of actors

The data is loaded into memory using `load_data(directory)`.

The main function then:

1. Loads the dataset (`small` or `large`)
2. Prompts for two actor names
3. Retrieves their IDs via `person_id_for_name()`
4. Computes the shortest connection using `shortest_path()`
5. Displays the degrees of separation and the connecting movies

---

## 🚀 Usage

```bash
$ python degrees.py large
Loading data...
Data loaded.
Name: Emma Watson
Name: Jennifer Lawrence
3 degrees of separation.
1: Emma Watson and Brendan Gleeson starred in Harry Potter and the Order of the Phoenix
2: Brendan Gleeson and Michael Fassbender starred in Trespass Against Us
3: Michael Fassbender and Jennifer Lawrence starred in X-Men: First Class
```

---

## 🧑‍💻 Getting Started

1. Clone the repository

   ```bash
   git clone https://github.com/yourusername/degrees.git
   cd degrees
   ```
2. Run the program

   ```bash
   python degrees.py small
   ```
3. Enter two actor names to find their degrees of separation!

---

## 🧠 Concepts Involved

* Graph representation of actor-movie relationships
* Breadth-first search (BFS) algorithm
* Data loading and mapping with Python dictionaries
* Command-line interaction

---

## 📚 Acknowledgements

PSET0 **CS50’s Introduction to Artificial Intelligence with Python** 
---
