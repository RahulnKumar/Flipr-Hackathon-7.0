# Flipr-Hackathon-7.0
The objective of the problem statement is to predict Total runs of a player in IPL 2020

### FILES DESCRIPTION  
1. DATA : CONTAINS ALL THE CSV/XLSX FILES
2. SOLUTION : CONTAINS SOLUTION CSV AND DOC FILE
3. EDA.ipynb : All the preprocessing, eda stuff, like which features is most important etc stuff is in this notebook.
4. Feature_engineering.ipynb : In this notebook, all the new featueres has been created
5. Train_Test.ipynb : Actual train and testing has been done in this notbook.

### EXPLANATION  

I used simple linear regression for my model.
At first I tried with simple neural network with one or two  hidden layers but that didn’t give good results.  
Explanation  (features I used) :
For getting estimate of player next year total run , the most important feature is a player’s consistency and which can be obtained using his previous year scores and at least 2-3 years records.  But since only 1 year data we were suppose to use. So we can’t get consistency as features. So I made features using the data provided.
And instead of using 12 feautures as provided to us. I used my own 3 features which I derived from those 12 features based on my cricket knowledge. And those features are:

1. Class of batsman(0,1,2,3)  
 If a batsman has played more than 10  matches and scored less than 100 runs  and not out is greater than 2, I classified them as class 0, if runs  more than 500 then class 1. So class 0 or 1 = Tail enders  and class 2 or 3  = Middle order or top  order bats man  
So more is the class more run he will score.    

Class(0,1,2,3) = function of (no. of innings played, no. of not outs, runs scored)   

2. Form of the batsman  
 This feature I manipulate from the percentage of run a players scores from
 boundaries. If a person is in form then higher percentage of run will be from 
 boundaries.  

 Form = (4*(no. Of fours)  + 6*(no. Of sixes))/(total runs scored)  
  

3. Total runs scored :  
     This is most important feature although we don’t have idea for a player consistency  from just one year records.  


Also its almost impossible to predict what a player will score next year from just one 
years stats. So the prediction for this type of problem doesn’t  depend much on the model used, rather on what features the model is trained.

I didn’t used features such as highest score, avg score because those really doesn’t give a clue about a player’s total score and some of then are depended on total runs scored. So I used my own features and got the following accuracy while training and testing on the 2019 data.  
Training accuracy : 98.17 %  
Testing accuracy  :  97.82  

            -----------------“ Form is temporary but Class is permanent ”----------------
            
            
### Contributors  
 - Rahul Kumar
 ### License & copyright
 © 2020 Rahul Kumar   
 Licensed under the [MIT License](LICENSE)


