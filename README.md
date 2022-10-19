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

### - What are the advantages or disadvantages of refactoring code?

Included in this repository is a Python script that can process similarly structured CSV files and provide the same types of summary statistics.  Assumptions about the structure of the data file in order for the script to run properly and provide identical summary statistics:
1. The provided file is named "election_results.csv" and saved in the Resources directory of the repository prior to running the code.
2. The first row of the CSV file contains header detail about subsequent rows (column headers) and does not contain actual data.
3. Column 2 of the file contains the name of the County in which the vote was cast.
4. Column 3 contains the name of the candidate for whom the ballot was cast.

