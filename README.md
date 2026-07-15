## Python Setup
1. Install dependencies:
pip install -r requirements.txt

2. Ensure Jupyter Book is on version 1:
jupyter-book --version

✅ Jupyter Book      : 1.0.4.post1

or similar

3. Run Jupyter Book:
jupyter-book clean .
jupyter-book build .

4. Run the Jupyter Book Server:
python -m http.server --directory _build/html

5. Open the localhost server hyperlink or by typing into a web browser:
http://localhost:8000