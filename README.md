# Election Analysis

## Election Analysis Project Overview
I was asked to assist in performing an analysis on a recent U.S congressional elections race by the Colorado Board of Elections. While somebody could easily perform all the same analysis using nothing more than excel, I was asked to create a tool that could repeat the process in an automated manor. In order to do meet this demand I decided to build the workflow using Python within the Visual Studio Code program. I chose this because Python is one of the most universal and widely used programming languages. This means that most any other analysts that review my work in the future would be able to understand how I wrote it, in case they needed to troubleshoot a problem. It also adds the flexibility for any analysts to quickly alter the code if they wanted to extract different data points.

---

## Deliverables

There were several important key pieces of information that needed to be evaluated in order to conduct an accurate analysis of the raw voting data. The Board of Elections provided a very specific list of the things they would like me to create and display for them.

1. Overall total number of votes
2. Total number of votes by
3. Overall percentage of votes by county
4. Identify county with largest voter turnout 
5. Total votes by candidate
6. Percentage of votes by candidate
7. Winning candidate 
8. Winner total votes
9. Winner total vote percentage

All these requirements needed to be not only displayed in the command line of any user that ran the code but the board also wanted a .txt file created after the analysis script was run. This allows the flexibility of saving and possibly sending out the results of the analysis.

## Analysis

In order to accomplish the requirements I first had to come up with a list of tasks I would need to perform to achieve the desired results.

1. The first important step was to load the raw election data from a CSV file. Below is a the code I used to accomplish this:

 ![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/import%20csv.png)
 
2. Next I needed to loop through the county and candidate votes to total them. I did that by using ``for`` loops. Below is an example of the ``for`` loop I used for the county information:
 
 ![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/Screenshot%202022-12-21%20at%208.31.55%20AM.png)
 
3. Now that I had gathered and summed all the votes, I needed to display the percentage of votes that each county and candidate received in relation to the total counts. This was accomplished by creating a simple equation of dividing the totals by 100:

``vote_percentage = float(votes) / float(total_votes) * 100``

4. The last, most important task was to create an output that would present the results in an organized and clean format in the command line. To do this I used various ``f strings`` in order to incorporate both string and integers.

![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/Screenshot%202022-12-21%20at%208.31.31%20AM.png)

---

## Results

The results were presented not only on the winner but the rest of election results by candidate and county.

Based on the below results, the overall outcome highlights 
are the following:

1. The winner was Diana DeGette with 272,892 votes. She received 73.8% of all votes.
2. The County with the highest voter turnout was Denver county with 82.8% of all votes. 
3. The runner-up candidate was Charles Casper Stockham. Charles received a total of 23.0% of the total votes which equated to 85,213.

![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/Screenshot%202022-12-21%20at%208.33.20%20AM.png)

![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/Screenshot%202022-12-21%20at%208.33.29%20AM.png)

![](https://github.com/TONY-H83/Election_Analysis/blob/main/Resources/Screenshot%202022-12-21%20at%208.33.37%20AM.png)

---

## Summary

This was great way to demonstrate just how useful building out a Python script can be. This analysis could have been done directly in Excel but it would have taken several different pivot tables, formulas, and lost of manual manipulation of the raw data. The manual touch points also introduce the possibility of human error as this manual work would need to be done every time a change or update needs to be made. Creating a Python script to automate the analysis means that it can be used over and over in the coming years. It can also be easily modified and repurposed. This exercise was very useful as it not only helped me create my first script in Python but also perform input and write functions.
