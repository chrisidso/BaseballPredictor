# BaseballPredictor

The idea for this project was to predict whether a player on the roster of a MLB team
at the end of a given season would still be on the roster at the start of the next season.

I found a seemingly handy python module with which one can get baseball information, but its documentation was incomplete.  The documentation contained a list of functions to call, which are designed to be called in sequence, but there were more functions than examples. This meant that I had to perform some experiments in order to determine which information I could get and how to get it.  

Following the sequence I was able to get a list of the teams and their identifying codes, and then the roster for a given team, and then general player information for each player.  But I could not figure out how to get statistics for each player.  

The experiments I performed and my eforts to get statistics for each player took time, and eventually I had to stop and turn to creating models using the data I had. In the end I had a model with only two features; the age of the player and the length of time (in years) spent in the major leagues. 

The data itself caused problems too:
1) The data comes in the form of a list of dictionaries, and some of the values in the dictionary are themselves dictionaries.  
2) There are empty spaces where one would not expect them ... such as some players apparently do not have a jersey number.
3) Retrieving the 40 man roster for a team for a given year (you can get this for the start or end of the year) does not necessarily result in a list of 40 players. 

I have added some notes to the jupyter notebook I was working in, to describe in greater details the steps I had to go through to retrieve the data, assemble the datasets I heeded, and create the target data (consisting of ones and zeros). 

I do not think I will continue this project into my third capstone, unless I can figure out how to get the information I need (statistics, maybe contract/salary information) and how to mix it in with information I already have.

There are two data files.  
https://ci-baseballpredictor.s3.us-east-2.amazonaws.com/roster2017final
https://ci-baseballpredictor.s3.us-east-2.amazonaws.com/roster2018final

The notebook called Baseball1.ipynb loads these files. You can load that notebook and run it. The other notebook - baseball2.ipynb - has my code in it but it will probably not run.

