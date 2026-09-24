# Covid tracking dashboard

This dashboard displays data about Covid-19, using data from the UK Health Security Agency (UKHSA).

## Project file

- `/home/runner/work/Covid-tracking-dashboard/Covid-tracking-dashboard/Covid Tracking Dashboard.ipynb`

## Run the interactive dashboard locally (Jupyter)

1. Open a terminal in `/home/runner/work/Covid-tracking-dashboard/Covid-tracking-dashboard`.
2. Install dependencies:
   - `python -m pip install -r requirements.txt`
3. Start Jupyter:
   - `jupyter lab`
   - or `jupyter notebook`
4. Open `Covid Tracking Dashboard.ipynb`.
5. Run all cells so the widget controls and graphs are displayed.

## Ensure widget support

- If widget controls do not render, install/upgrade ipywidgets:
  - `python -m pip install -U ipywidgets`
- For classic Notebook, enable widgets if needed:
  - `jupyter nbextension enable --py widgetsnbextension`

## Publish as a browser app with Voilà

1. From `/home/runner/work/Covid-tracking-dashboard/Covid-tracking-dashboard`, run:
   - `voila "Covid Tracking Dashboard.ipynb" --port=8866 --no-browser`
2. Open the local URL printed in the terminal.

## Export non-interactive output

- Static HTML:
  - `jupyter nbconvert --to html "Covid Tracking Dashboard.ipynb"`
- PDF (if LaTeX is available):
  - `jupyter nbconvert --to pdf "Covid Tracking Dashboard.ipynb"`
