# Python Setup
1. Install dependencies:
pip install -r requirements.txt

# Jupyter Book Setup
1. Ensure Jupyter Book is on version 1:
jupyter-book --version

The terminal results should be:
Jupyter Book      : 1.0.4.post1

2. Compile Jupyter Book:
jupyter-book build .

3. Run the Jupyter Book Server:
python -m http.server --directory _build/html

4. Open the localhost server hyperlink or by typing into a web browser:
http://localhost:8000