# Kickstarting with Excel

## Challenge Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.
1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular votes.

## Election-Audit Results:
The analysis of the election show that:

* There were 369,711 votes cast in the election.
* The candidates were:
	* Charles Casper Stockham
	* Diana DeGette
	* Raymon Anthony Doane
* The candidate results were:
	* Charles Casper Stockham received 23.0% and 85,213 votes
	* Diana DeGette received 73.8% and 272,892 votes
	* Raymon Anthony Doane received 3.1% and 11,606 votes
* The winner of the election was:
	Diana DeGette who received 73.8% and 272,892 votes
	
![2018 ReturnsDeliverable_1_print_to_command_line](https://github.com/cortesh/Election_Analysis/blob/main/Resources/Deliverable_1_print_to_command_line.png)

## Challenge Summary - Election-Audit Summary: 

It is the finding of this study that with minor changes to the script, it can be reused to tabulate local elections along with county wide and state wide elections.

For example.  Currently, results are tabulated by candidate in a state wide race across multiple counties.  However, for smaller elections, it is not sufficient to determine which candidate received the most votes statewide irrespective of the county.  It will be necessary to create a nest for loop to run through each precinct and the candidates within each precinct before looping through the next candidate.  

First a variable would hold the precinct similar to this:

```
        # 3: Extract the county name from each row.
        county_name = row[1]
```

Except here it would read:

```
        # 3: Extract the county name from each row.
        precinct_name = row[1]

```

Then one would iterate through these precincts for the winner using the same code.

Another consideration may be to test participation of each county as a share of their weight based on registered voters in order to determine turnout percentage.  For this, such registered voter data would have to be supplemented to the results but should be widely available.

