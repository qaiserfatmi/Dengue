# Dengue

This is a basic and a quick analysis where machine learning models was developed using routinely collected demographic, clinical, laboratory, and environmental variables that demonstrated moderate capability for predicting dengue infection prior to molecular confirmation. Random Forest provided the highest predictive performance, whereas Logistic Regression achieved comparable discrimination with greater robustness across cross-validation folds. These findings suggest that machine learning may serve as a useful decision-support tool for early dengue diagnosis, particularly in resource-limited settings where rapid molecular testing is unavailable. Further validation using larger multicenter cohorts is warranted to improve generalizability and clinical applicability.

# Use following command to directly upload the journal.pntd.0012978.s006.xlxs file from website

import pandas as pd

import requests

url = "https://journals.plos.org/plosntds/article/file?type=supplementary&id=10.1371/journal.pntd.0012978.s006"

r = requests.get(url)

r.raise_for_status()

with open("journal.pntd.0012978.s006.xlsx", "wb") as f:

    f.write(r.content)

df = pd.read_excel("journal.pntd.0012978.s006.xlsx")

df.head()
