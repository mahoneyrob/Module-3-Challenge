# Overview of Project
The purpose of this project was to help Seth and Tom, two elections officials in Colorado, help analyze election data and determine the winner of a local election.

## Results: 

### Audit Results:
The audit results showed the following

There were 369,711 total votes cast over 3 counties.<br>

	 -Denver county had the most voters vote, with 306,055 votes, or 82.8% of the total vote.
	 -Jefferson county had the next most, with 38,855 votes, or 10.5% of the total vote.
	 -Arapahoe county had the fewest votes cast, with 24,801 votes, or 6.7% of the total vote.

There were 3 candidates that received votes.<br>

	 -Diana DeGette received the most votes and won the election, with 272,892, or 73.8% of the vote. 
	 -Charles Casper Stockham received the second most votes, with 85,213, or 23.0% of the vote. 
	 -Raymon Anthony Doane received the fewest votes, with 11,606, or 3.1% of the vote. 


### Audit Summary

In the future, this script appears to be able to be used as is in almost any election.  Provided that the data is organized as a csv, with the first column as voter id (although this does not matter as it is not used), second as county where the ballot is cast, and third as candidate voted for, the import of the code does not need to be modified.  The lists and dictionaries that are being used are not a finite size, so if there were more or fewer candidate, the code would still store those candidates.  This is also true if there were more than 3 counties that have votes to be counted.  I don't believe that the code really needs to be modified for other elections, unless there are different column values in the csv than we have used.  

The number of votes cast is stored in a list, and vote count for each candidate is determined by increasing the count for each candidate in a dictionary.  This is also done for the counties in determining how many votes were cast in each county.  Because of the "if" statements that determine if a candidate or a county is not in the list, we are collecting the unique values for the candidates and counties to be stored in a list.  We then go through the list with a for loop, looking at each candidate and county individually, and count the times that the candidate or county appear in the data.  We store this in a dictionary, with either the candidate or the county as the key, and the votes as the value.  We are able to determine a winner by using an if statement to compare the votes for the candidate or county to the most votes for the previous candidates.  If the vote count is less, the previous candidate is still in the lead, if it is more, the new candidate is replaced as the winner.  After that, all of the data is printed in the terminal, as well as outputted to a text file.  Below are the results I found when executing the script.


#Election Results

##Total Votes:

####369,711


##County Votes:

####Jefferson: 10.5% (38,855)

####Denver: 82.8% (306,055)

####Arapahoe: 6.7% (24,801)



##Largest County Turnout:

####Denver


##Candidate Votes:

####Charles Casper Stockham: 23.0% (85,213)

####Diana DeGette: 73.8% (272,892)

####Raymon Anthony Doane: 3.1% (11,606)



##Outcome:

####Winner: Diana DeGette

####Winning Vote Count: 272,892

####Winning Percentage: 73.8%

