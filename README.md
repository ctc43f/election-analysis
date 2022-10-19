# Election Audit

## Overview of Election Audit
The election commission provided us with a raw data file containing ballot-level detail of votes cast in the recent congressional election.  The commission asked us to provide summary statistics for the raw data at both a candidate and district level, as well as to provide a method for automating the analysis of similarly structured data files that could then be applied to other raw data provided in the future.

## Election Audit Results
Below are images containing the summary statistics requested by the election commission:

**Total Votes Cast in Election**

![Image 1: Total Votes Cast](/Resources/total_votes_cast.PNG)

**Vote Count and Percent of Total by County**

![Image 2: Vote Detail by County](/Resources/votes_by_county.PNG)

**County with Largest Turnout**

![Image 3: County with Largest Vote Count](/Resources/largest_county.PNG)

**Vote Count and Percent of Total by Candidate**

![Image 4: Vote Detail by Candidate](/Resources/candidate_breakdown.PNG)

**Winning Candidate Summary Statistics**

![Image 5: Winning Candidate Detail](/Resources/winning_candidate.PNG)

## Election Audit Summary

### How to repurpose the Python Script as-is
The provided script can be be applied to any similarly structured data file containing ballot-level detail.  In order to apply the Python script to the file, it can be placed in the Resources folder of this repository; running the Python script will generate a results file in the Analysis folder.  This assumes the following about the file:

1. The file used is a properly constructed CSV file titled election.results.csv.
2. The first row of data in the file contains the column names for the subsequent rows of data.
3. Each row represents a single ballot/a single vote cast.
4. Columns 2 and 3 of the file contain county in which the vote was cast and candidate for whom the vote was cast, respectively.


### Modifying the script if columns in data are rearranged
If the file contains vote-level data but the structure of the file is different, the below modifications will need to be made:
- If the candidate name is in a different column, line 48 of the code will need to be modified.  Specifically, the number in brackets will need to be modified such that the number is one less than the column number in which the name appears.  If, for example, the Candidate Name was the first column in the data, the line should instead read:
```
candidate_name = row[0]
```
- Similarly, if the County is in column 11 of the CSV file, line 51 should read:
```
county_name = row[10]
```
The script is written such that it is agnostic to any other data that might be present in future files.  As long as the user redirects the script to point to the correct columns for name and county, it will generate the same summary statistics regardless of the content of other columns.

### Future Modifications: Providing counts by candidate and district

In the above we provided vote breakdown by candidate and county, independent of one another.  We could also look at breakdowns of vote by candidate and county to gain insights into where each candidate's core base resides.  In the Python script we used dictionaries to hold each county/candidate and corresponding vote count, we could instead create a nested dictionary for each candidate and rewrite a single if statement that checks whether or not a given county dictionary exists in the dictionary of said candidate and then add as needed or modify the vote count for that candidate/county combination.  (Note: this can also be accomplished more easily by using a Pandas Dataframe to create a summary statistics dataframe via if statement, which we will cover next week).
