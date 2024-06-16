# Pearl Jam Concert Dashboard

This dashboard leverages setlist data collected from setlist.fm using Python and BeautifulSoup. To ensure a comprehensive and organized data model, additional datasets were created for Pearl Jam’s albums, songs, tours, and concert venues.

## Measures

- **Average Concert Length**: Calculates the average "net" length of concerts within the selected period by summing the lengths of the songs listed in the setlist.
- **Longest Concert**: Identifies the longest concert within the selected period.
- **Longest Concert Location**: Provides the location data of the longest concert in the format "City, Country, Date."
- **Most Frequent Opening Song**: Determines the song most frequently used as the opening song in concerts during the selected period.
- **Number of Concerts**: Counts the number of shows within the selected period.
- **Times Played**: Counts the number of times a song was played within the selected period.

## Dashboard Pages

- **Statistics**: This page offers overall statistics about the concerts, filtered by a date slicer. It includes a bar chart showing the number of shows and a shape map of visited countries, both of which also function as filters. The "Times Played" bar chart includes a tooltip that displays the song’s album cover and a yearly stat of times played when you hover over the song's name.

- **Tour**: This page filters the concert data by date and by tour. The map visualization includes a tooltip that shows the setlist of each concert when you hover over it. In cases where multiple concerts occurred in the same year and location, setlists were duplicated. To resolve this, a modified latitude and longitude column was created in the Venues table by truncating the end of the coordinates. A UniqueConcerts calculated table was then created using the original concert indexes from the Concerts table and the modified coordinates from the Venues table. A random number was added to the end of each coordinate, ensuring that concerts at the same location have distinct coordinates, thus creating unique points on the map in Power BI.

