<p align="center">
  <img src="https://github.com/user-attachments/assets/bc734d7c-b501-4786-9ffc-4f801d859ee8" width="794" height="400" />
</p>


## <b>Overview</b>

The **Sanremo Music Festival** is Italy’s most prestigious and long-running music competition, first held in 1951 and broadcast annually on national television. Over the decades, it has played a central role in shaping Italian popular music and cultural trends.

This dataset provides a structured and curated view of the Sanremo Music Festival main competition, covering **songs**, **performing artists**, **song authors**, and **final results** across editions.

Please note that only entries from the "main" category are included. Songs competing in “Newcomers”, “Giovani”, or “Nuove Proposte” sections are **not included**.

The dataset is built from publicly available sources, cleaned and normalized to support data analysis, visualization, historical research, and machine learning applications.

It is designed as a living dataset and will be **updated annually** after each new edition of the Sanremo Music Festival.

-------

## <b>Dataset Structure</b>

<b>`year`</b> : Year of the Sanremo Music Festival edition<br><br>

<b>`placement`</b> : Final competition result or participation status.<br>
Possible values are:<br>
    <b>1, 2, 3, …</b> : Final ranking position in the competition<br>
    <b>F</b> : Finalist (qualified for the final stage)<br>
    <b>NF</b> : Not Finalist (did not qualify for the final stage)<br>
    <b>DQ</b> : Disqualified<br>
    <b>RT</b> : Retired (withdrew from the competition)<br><br>

<b>`artist`</b> : Name of the performing artist or artistic unit as officially presented at the festival<br><br>

<b>`artist_id`</b> : Unique identifier for the artist or artistic unit<br><br>

<b>`song`</b> : Song title<br><br>

<b>`song_id`</b> : Unique identifier for the song<br><br>

<b>`author`</b> : Song author(s)


-------

## <b>Notes</b>

Until 1971, with the exception of 1956, each song competing at the Sanremo Music Festival was traditionally performed by two different artists.
For this reason, the same song may appear multiple times in the dataset, each associated with a different artist.
This behavior is intentional and historically accurate, and does not represent a data duplication error, as the `song_id` field can be used to identify and group identical songs across different performers.

Artist entities are not split when performers officially appeared at the festival as a single artistic unit.
Groups, collaborations, or combined credits are treated as one unique artist, exactly as they were presented on the official Sanremo stage (for example, "Nilla Pizzi e Duo Fasano" is considered a single artist entity).

-------

## License

This dataset is released under the Creative Commons Attribution 4.0
International (CC BY 4.0) license.
