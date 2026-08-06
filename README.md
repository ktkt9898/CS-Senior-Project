# Python Setup
1. Install dependencies:
pip install -r requirements.txt

2. Ensure Jupyter Book is on version 1:
jupyter-book --version

✅ Jupyter Book      : 1.0.4.post1

or similar

3. Compile Jupyter Book:
jupyter-book build .

4. Run the Jupyter Book Server:
python -m http.server --directory _build/html

5. Open the localhost server hyperlink or by typing into a web browser:
http://localhost:8000

# Data Overview
* The senate.csv is compiled on a recurring basis, usually daily, by the New York Times and consists of the most recent and accurate data provided by reputable pollsters such as YouGov, Quantus Insights, and the University of Massachussetts.
The important columns in the document are the state, sample size, party, and answer. These values are used in the prediction analysis to compile data to generate the most likely results for each senate race.

* The baseline data is compiled from historical races to generate a basic starting position on how a senate race was previously won to better understand voter indication.