# Linux-Terminal-Command-practice
Description
1. Filter 1 column from a CSV file. Extract out the artist names from the CSV file that can be downloaded from the Spotify Charts website (https://spotifycharts.com/regional). Ensure that the artist names are unique and sorted. Retain the header as the top of the file.

Please see <b>log5-1.txt</b>

The following sequential commands were used to preview the filtered and sorted result with no duplicates:

awk -F , '{print $3}' chart.csv | head -n1; awk -F , '{print $3}' chart.csv | tail -n+2 | sort -u

The following sequential commands were used to write the result to a text file:

(awk -F , '{print $3}' chart.csv | head -n1; awk -F , '{print $3}' chart.csv | tail -n+2 | sort -u) >output.txt


2. Download a zip file from MovieLens (https://grouplens.org/datasets/movielens/latest/) using the command line interface (CLI) such as curl or wget and unzip the .zip file. It would be okay to choose the smallest (recent data) dataset.
3. Preview the first 12 lines of the movies.csv file and the last 4 lines of that same csv file.
