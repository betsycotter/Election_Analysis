# Election Analysis

## Overview of Election Audit

Our clients, Tom and Seth, work for the Colorado Board of Elections. They have asked us to review some results from a recent election in a U.S. congressional precinct in Colorado. They would like to know the total number of votes, as well as summaries for the county votes and for the candidate votes, including their individual totals and percent to totals. They have requested help in automating this process using Python, so that they can use the code for other elections. 

## Resources
- Data source: election_results.csv
- Software: Python 3.9.12, Visual Studio Code 1.73.0

## Election Audit Results 

Based on our analysis, the results are as follows: 

- The total number of votes cast was 369,711 votes 
- Votes based on county: 
  - Jefferson voters cast 10.5% of the votes or 38,855 number of votes
  - Denver voters cast 82.8% of the votes or 306,055 number of votes
  - Arapahoe voters cast 6.7% of the votes or 24,801 number of votes
- Denver county had the largest number of votes cast
- Votes based on candidate: 
  - Charles Casper Stockham received 23.0% of the votes or 85,213 number of votes
  - Diana DeGette received 73.8% of the votes or 272,892 number of votes
  - Raymon Anthony Doane received 3.1% of the votes or 11,606 number of votes
- Diana DeGette was the winner of the election with 272,892 votes, which was 73.8% of the total votes

Results are also displayed below: 

<img width="307" alt="Election_Results" src="https://user-images.githubusercontent.com/116031639/200935651-fea837f5-78cd-4b2d-8d8a-88d0ba51bc47.png">

## Election Audit Summary

Per the original requirements, we have created a script that can be modified for future use. The script currently pulls from the [election_results.csv](Resources/election_results.csv) file. In the future, the script can be modified in the following areas: 

`file_to_load = os.path.join( "Resources", "election_results.csv")`

`file_to_save = os.path.join("analysis", "election_analysis.txt")`

The team will need to update the file path and file name, as necessary. With the updates to the above script, the correct files will be pulled and saved throughout the rest of the script. 

Furthermore, the script currently runs data to pull from the county and candidate columns. If there are additional columns or the columns are swapped, there can be changes made in the following areas: 

`county_name = row[1]`
or
`candidate_name = row[2]`

In the current file, county is in the second column which is index 1 and the candidate name is in the third column which is index 2. The current index numbers 1 and 2 can be updated appropriately.

Note: if the columns are swapped or there is additional data to pull, the variable, lists, and dictionary names will likely need to be updated as well, for clarity. If this is the case, the user can find and replace the names of the items to be replaced. 

The overall script is shared with the election commission via this [GitHub Repository](https://github.com/betsycotter/Election_Analysis). The election commission will be able to make adjustments and find the data that they need for future elections. 
