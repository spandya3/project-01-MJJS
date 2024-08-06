# project-01-MJJS
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "1edabd26-b5e1-4e8f-a6ed-c1e24cc87a68",
   "metadata": {},
   "outputs": [],
   "source": [
    "import matplotlib.pyplot as plt\n",
    "import pandas as pd\n",
    "import numpy as np"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "id": "76828c82-8a76-4bc6-84e3-81289eb6b792",
   "metadata": {},
   "outputs": [],
   "source": [
    "\n",
    "movie_data = pd.read_csv(\"imdb-movies-dataset.csv\")\n",
    "movie_data_df = pd.DataFrame(movie_data)\n",
    "dropped_empty_df = movie_data_df.dropna(how='any')\n",
    "\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 68,
   "id": "3bbb77fa-61dc-4793-b3c3-3ef580cab685",
   "metadata": {},
   "outputs": [],
   "source": [
    "dropped_empty_df.to_csv(\"./clean_movie_data.csv\", index=False, header=True)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "6570a48a-083b-4273-8075-47ac02b55565",
   "metadata": {},
   "outputs": [],
   "source": []
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
   "version": "3.12.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
