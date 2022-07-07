# Election Analysis
## July 7, 2022

#### **Purpose**
The purpose of this project was to breakdown and analyze a congressional election by counties. This break down shows what county voting turnout(numbers and percentage). Additionally, it shows which candidate won the election by raw numbers and a percentage of the total votes. 

#### **Results**
Overall, 368,711 votes were cast  in three counties. Denver, which had the highest percentage of voters at 82.8 percent of the total votes or 306,055 number of votes had the largest voter turnout. Jefferson was second at 38,855(10.5%). Last, Araphoe had around 24,801 votes, or 6.7%. Candidate Diana Degette was the winner of the lecetion who had 272,892 votes, or 73.8%. Next, Charles Casper Stockham came in at 85,213 votes(23%), In last place, Raymon Anthony Doane took 3.1% of all votes (11,606). [^1]
#### **Summary**
As is, this information is not very useful beyond providing the successful candidate. The first modification to make is to get a true voter turnout by county. The current code finds a percentage, *Cvote_percentage= float(C_votes)/float(total_votes)*100*, where variable,*C_votes*, is the number of county votes and the variable, *total_votes*, is the total number votes in the election. This *total_votes* is the incorrect variable to use in this instance and does not show voter turnout, but how many votes were from people in Denver. The correct way to capture voter turnout by County would be the equation *Cvote_percentage= float(C_votes)/float(county_voters)*100*, where county_voters would reflect the number of eligible voters of the desired county of interest. For example lets say we use some arbitrary variable where:  

-total votes of precinct:1000  
-Denver votes: 700  
-Denver Eligible Voters:1400  
-Jefferson votes:300  
-Jefferson Eligible Voters:300  

Let's first use the formula used in the homework:*Cvote_percentage= float(C_votes)/float(total_votes)*100*  
-Denver:700/1000 multiplied by 100= **70%**  
-Jefferson:300/1000 multiplied by 100= **30**  
-Based on the challenge assignment, we would say Denver had the greatest voter turnout. Now, let's use a more accurate formula.  

More Accurate Formula:*Cvote_percentage= float(C_votes)/float(county_voters)*100*  
-Denver:700/1400 multiplied by 100= **50%**  
-Jefferson:300/300 multiplied by 100= **100%**  
-Based on this equation, Jefferson actually had higher voter turnout.   

This is important, because we do not want to misrepresent data. If the county government were trying to improve voter turnout, then Jefferson might have believed they had a major problem with getting voters to the polls. In actuality, their community is highly involved in politics and casting their votes. This is one way the code could be modified and used for informational purposes. 

Another modification could be to show the number of votes for each candidate in each county. Then, the candidates could see which county they are doing well or poorly in. This would be an even simpler modification, where you total the votes of each county and then find the percentage for each candidate.    

[^1]:![the votes breakdown](https://github.com/encollin94/python-project/blob/main/election_results.png)
 
