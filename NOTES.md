# Notes

- https://letterboxd.com/api-beta/
- https://letterboxd.com/settings/data/
- https://api-docs.letterboxd.com/
- [Rows](https://rows.com/docs) documentation:
  - [Charts](https://rows.com/docs/category/charts): [Inserting and editing charts](https://rows.com/docs/ch-inserting-editing-charts?category=charts) page
- https://help.flourish.studio/article/49-changing-the-format-of-your-data-with-pivot-tables
- https://rows.com/share/my-letterboxd-10wBKefPuzblIiLcelgERRcNnjh8JeTXmUuVz5RgzQEa
- "Stats and charts from my [Letterboxd](https://letterboxd.com/) movie history."
- https://github.com/joaopalmeiro/podcasts-backup
- https://github.com/Dashron/letterboxd-client:
  - https://github.com/Dashron/letterboxd-client/blob/1.0.1/src/index.ts#L80

## Snippets

### `dev.ipynb` file

```json
{
  "cells": [
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "5840790b-5330-44bd-b205-c5c5e1afed78",
      "metadata": {},
      "outputs": [],
      "source": ["import pandas as pd"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "c1cd9fbd-13be-45d9-a435-01b3fe66ec01",
      "metadata": {},
      "outputs": [],
      "source": ["DATA: str = \"data/diary.csv\""]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "54d57623-330d-4ae8-80b1-4d400109e909",
      "metadata": {},
      "outputs": [],
      "source": ["df = pd.read_csv(DATA)"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "f048f771-7e1d-4816-bbcd-c72798957f53",
      "metadata": {},
      "outputs": [],
      "source": ["df.head()"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "10e363fd-0d78-4206-8df1-09e1db9203ac",
      "metadata": {},
      "outputs": [],
      "source": ["df.shape"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "0711d75d-cfb4-4b9b-a374-be87d63b7a45",
      "metadata": {},
      "outputs": [],
      "source": ["df.dtypes"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "154f7877-313f-498e-80b3-d15b74356e36",
      "metadata": {},
      "outputs": [],
      "source": ["df[\"Tags\"].value_counts(dropna=False)"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "7857ca50-cb9a-4803-a0f1-e16690c1d579",
      "metadata": {},
      "outputs": [],
      "source": ["df[\"Year\"].value_counts(dropna=False)"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "e55a3f13-d08e-4e6f-b75f-59cf891ac334",
      "metadata": {},
      "outputs": [],
      "source": ["df.query(\"Tags == 'disney_plus'\")"]
    },
    {
      "cell_type": "code",
      "execution_count": null,
      "id": "5a2da841-14e5-4754-979d-bba648f9b31d",
      "metadata": {},
      "outputs": [],
      "source": [
        "export_cols = [\"Name\", \"Tags\", \"Watched Date\"]\n",
        "\n",
        "df[export_cols].to_csv(\"data/My Letterboxd.csv\", index=False)"
      ]
    },
    {
      "cell_type": "markdown",
      "id": "def466fc-2097-4ddd-8794-e76d0b77eccc",
      "metadata": {},
      "source": ["---"]
    }
  ],
  "metadata": {
    "kernelspec": {
      "display_name": "Python 3 (ipykernel)",
      "language": "python",
      "name": "python3"
    },
    "language_info": {
      "codemirror_mode": {
        "name": "ipython",
        "version": 3
      },
      "file_extension": ".py",
      "mimetype": "text/x-python",
      "name": "python",
      "nbconvert_exporter": "python",
      "pygments_lexer": "ipython3",
      "version": "3.7.12"
    }
  },
  "nbformat": 4,
  "nbformat_minor": 5
}
```
