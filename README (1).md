# TOPSIS Web Service

This project is a Flask-based web application that implements the TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) method.
It allows users to upload a CSV file through a web interface and receive the TOPSIS results via email.

This web service was developed as part of a data science assignment to demonstrate algorithm implementation, backend development, and automation.

---

## Overview

The application provides a simple browser-based interface where users can:

- Upload a CSV file containing alternatives and criteria
- Enter weights for each criterion
- Specify impacts (`+` for benefit, `-` for cost)
- Provide an email ID to receive the output

After processing, the system calculates TOPSIS scores and ranks, generates a result CSV file, and emails it to the user.

---

## How the Application Works

1. User uploads a CSV file through the web interface.
2. User enters weights, impacts, and an email address.
3. Input data is validated by the backend.
4. TOPSIS calculations are performed.
5. A result CSV file is generated.
6. The result file is sent to the user via email.

---

## Input File Requirements

- File format must be CSV
- First column should contain alternative names
- All columns from the second column onwards must be numeric
- The file must contain at least 3 columns

---

## Validations Performed

- Ensures a file is uploaded
- Confirms the file format is CSV
- Checks for sufficient number of columns
- Verifies numeric data in criteria columns
- Ensures weights count matches number of criteria
- Ensures impacts count matches number of criteria
- Accepts only `+` or `-` as valid impacts

---

## TOPSIS Methodology

The following steps are followed:

1. Normalization of the decision matrix
2. Application of user-defined weights
3. Identification of ideal best and ideal worst solutions
4. Calculation of Euclidean distances
5. Computation of TOPSIS score
6. Ranking of alternatives (Rank 1 is the best)

---

## Technologies Used

- Python 3.x
- Flask
- Pandas
- NumPy
- SMTP for email functionality

---

## How to Run the Application

1. Install required libraries:
   pip install flask pandas numpy

2. Run the Flask application:
   python app.py

3. Open the browser and visit:
   http://127.0.0.1:5000/

---

## Output

- A CSV file containing:
  - TOPSIS Score
  - Rank of each alternative
- The output file is automatically emailed to the user.

---

## Purpose of the Project

This project demonstrates:

- Practical implementation of the TOPSIS algorithm
- Web application development using Flask
- Input validation and file handling
- Automated result delivery via email

---

## Note

This project is intended for academic and learning purposes only.
