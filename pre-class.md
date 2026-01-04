# **Pre-Class Materials: Lesson 1.7 \- Introduction to Pandas**

## **1\. Setup Instructions**

Ensure your development environment is ready before class starts:

* **Environment:** Activate your `pds` conda environment.  
* **Libraries:** You should have `pandas` and `numpy` installed. If not, run:

```
conda install pandas numpy
```

* **Files:** Download `pandas_lesson.ipynb` from the course portal and place it in your `notebooks/` folder.

## **2\. Prerequisites (Assumed Knowledge)**

This lesson builds directly on your previous NumPy session. You should be comfortable with:

* Creating NumPy arrays (`np.array`, `np.arange`).  
* Understanding array shapes and dimensions.  
* Basic Python dictionaries (keys and values).  
* Python slicing notation (`[start:stop]`).

## **3\. Intro Reading: Why Pandas? (300 words)**

While NumPy is the king of numerical arrays, it lacks one thing essential for real-world data: **Context**.

Imagine a dataset of housing prices. In NumPy, it's just a matrix of numbers. You have to remember that "Column 0 is the square footage" and "Column 1 is the number of bedrooms." If you delete a column or reorder the rows, you might lose track of what the numbers represent.

**Pandas adds the labels.** It introduces the **DataFrame**, which is essentially a programmable Excel spreadsheet. Every row and every column has a name (an Index). This "Label-based" approach makes your code:

1. **Readable:** Instead of `data[:, 5]`, you write `data['Price']`.  
2. **Safe:** If you add two datasets together, Pandas doesn't just add them by position; it aligns them by their labels. If 'User\_A' is at Row 0 in one table and Row 10 in another, Pandas finds 'User\_A' in both and adds them correctly.

In this lesson, we will move from thinking in "indices" (0, 1, 2\) to thinking in "labels" (Name, Date, Price).

