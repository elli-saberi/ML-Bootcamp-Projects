# Project 02: Calculating City Distances from Tehran using Haversine Formula

This project demonstrates how to calculate the geographical distance between over 40,000 cities worldwide and a single reference point (Tehran, Iran). The calculation is performed using the Haversine formula, which determines the great-circle distance between two points on a sphere given their longitudes and latitudes.

---

###  Project Goal

The primary objective is to enrich a dataset of cities with a new, valuable piece of information: the distance of each city from Tehran. This involves:

-   Implementing the Haversine formula in Python.
-   Applying this formula to every row in a large DataFrame using Pandas.
-   Converting geographical coordinates from degrees to radians for the calculation.
-   Sorting the final dataset to easily identify the closest and farthest cities.

---

### Technical Details: The Haversine Formula

The distance `d` between two points with latitude ($\phi$) and longitude ($\lambda$) is calculated using the following formulas.

First, an intermediate value `a` is calculated:
$$ a = \sin^2\left(\frac{\Delta\phi}{2}\right) + \cos(\phi_1) \cdot \cos(\phi_2) \cdot \sin^2\left(\frac{\Delta\lambda}{2}\right) $$

Then, the central angle `c` is found:
$$ c = 2 \cdot \operatorname{atan2}\left(\sqrt{a}, \sqrt{1-a}\right) $$

Finally, the distance `d` is:
$$ d = R \cdot c $$

Where:
-   **$R$**: The Earth’s radius (approximately **6371 km**).
-   **$\phi_1, \lambda_1$**: Latitude and Longitude of the first point (Tehran).
-   **$\phi_2, \lambda_2$**: Latitude and Longitude of the second point (the city).
-   **$\Delta\phi$**: The difference in latitude ($\phi_2 - \phi_1$).
-   **$\Delta\lambda$**: The difference in longitude ($\lambda_2 - \lambda_1$).

A custom Python function `haversine_from_teh` was created to encapsulate this logic.

---

### Technologies & Libraries

-   **Python 3.x**
-   **Pandas**: For data loading, manipulation, and applying the distance function.
-   **NumPy**: For mathematical operations, especially trigonometric functions and radian conversion.
-   **Jupyter Notebook**: For interactive analysis and development.

---

###  How to Run

1.  Clone this repository and navigate to the project directory.
2.  Ensure you have the required libraries: `pip install pandas numpy jupyterlab`.
3.  Launch Jupyter Notebook (`jupyter notebook`) and open the `.ipynb` file to view the step-by-step analysis.
