## Election Analysis Overview
This Project analyzed the election results for three counties Jefferson, Denver and Arapahoe. 
The data provided for the analysis performed identified the Total Votes, County Votes and percentage as well Winning County and Candidate Votes. 

## Election Audit results
How many votes were cast in this congressional election?
  
        total_votes = total_votes + 1
Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.

    election_results = (
        f"\nElection Results\n"
        f"-------------------------\n"
        f"Total Votes: {total_votes:,}\n"
        f"-------------------------\n\n"
        f"County Votes:\n")
    print(election_results, end="")

    txt_file.write(election_results)

    # 6a: Write a repetition statement to get the county from the county dictionary.
    for county_name in county_votes:
        # 6b: Retrieve the county vote count.
        county=county_votes.get(county_name)
        # 6c: Calculate the percent of total votes for the county.
        county_percentage=float(county)/float(total_votes)*100
        county_results=(f"{county_name}:{county_percentage:.1f}% ({county:,})\n")

            # 6d: Print the county results to the terminal.
        print(county_results, end="")
            # 6e: Save the county votes to a text file.
        txt_file.write(county_results)
            # 6f: Write a decision statement to determine the winning county and get its vote count.
        if (county>winning_count) and (county_percentage>winning_percentage):
            winning_count=county
            winning_county_candidate=county_name
            winning_percentage=county_percentage


Which county had the largest number of votes?

    winning_county_summary = (
        f"\n-------------------------\n"
        f"Largest County Turnout: {winning_county_candidate}\n"
        f"Winning County Vote: {winning_count:,}\n"
        f"Winning County Percentage: {winning_percentage:.1f}%\n"
        f"-------------------------\n\n"
        f"Candidate Percentage of Votes:\n"
        f"-------------------------\n")

    # 8: Save the county with the largest turnout to a text file.
    print(winning_county_summary)

Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.

        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage

    # Print the winning candidate (to terminal)
    winning_candidate_summary = (
        f"-------------------------\n"
        f"Winner: {winning_candidate}\n"
        f"Winning Vote Count: {winning_count:,}\n"
        f"Winning Percentage: {winning_percentage:.1f}%\n"
        f"-------------------------\n")
    print(winning_candidate_summary)
Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
	
## Election Audit Summary
Project is created with Python version 3.9 and using Visual Studio. The Election Commission may further utilize this information for multiple counties. Should age demographics be included in the data set,the voter demographic could be analyzed for each county. In addition, the script can be modified to be used for other elections with variations to calculate winning percentage, winning candidate, largest county turnout. 
