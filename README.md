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

The provided script can be be applied to any similarly structured data file containing ballot-level detail.  In order to apply the Python script to the file, it can be placed in the Resources folder of this repository; running the Python script will generate a results file in the Analysis folder.  This assumes the following about the file:

1. The file used is a properly constructed CSV file titled election.results.csv.
2. The first row of data in the file contains the column names for the subsequent rows of data.
3. Each row represents a single ballot/a single vote cast.
4. Columns 2 and 3 of the file contain county in which the vote was cast and candidate for whom the vote was cast, respectively.


