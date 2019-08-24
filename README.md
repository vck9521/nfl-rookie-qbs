# Predicting the Future Salary of NFL Quarterbacks under their Rookie Contracts
## by Vincent Kim

## Introduction 
The NFL is highly regarded as one of the most popular and competitive sports league worldwide. Filled with the most skilled football players, each team has one goal in mind: the Super Bowl. As an NFL franchise, a plethora of things are taken into account when building a football team that can achieve immense success. Argued as one of the most, if not the most important, position in the NFL is the quarterback. Every year, numerous college quarterbacks enlist into the annual NFL Draft in hopes of having their dreams realized of getting drafted by a team. Once drafted into the NFL, these rookie quarterbacks sign their contract, now spanning as a four year under the current CBA agreement. Once, their rookie contracts expire, these quarterbacks are free to sign a new contract with any team, usually cashing in a lot of money because of how valuable the quarterback position is. Thus, teams need to do a lot of research and invest in a franchise quarterback in order to ensure as much success and revenue to the organization. As a result, teams need to determine how valuable quarterbacks are and what statistics and characteristics dictate how much they should make. In this report, a study is conducted into figuring out what those key traits are that determine a quarterback’s worth once their rookie contracts expire.

## Literature Review & Economic Theory
In a study conducted by Christian Deutscher and Arne Buschemann in “Does Performance Consistency Pay Off Financially for Players”, they tackled on a similar topic to this report except more directed into soccer instead of American football. Using data for five consecutive seasons with about 34,413 observations, they used variables like goals, assists, shots, pass success percentage, and more. The following results that they got in their study was a regression model and concluded that those factors did affect players’ salary. 

Another study similar to this experiment is “Contract Length, Expected Surplus, and Specific Investments” by Meng-Chi Tang. Rather studying the financial aspect of NFL contracts, Tang explored the length of them. However, what was extremely interesting is the fact that Tang concluded that NFL players, particularly quarterbacks, ended up signing more lucrative and lengthy contracts with teams who had fewer wins and sold less tickets in their games. This was because less successful teams tend to offer much more cash to players in hopes of garnering success in the future. Furthermore, players who were drafted early tended to sign more lengthy contracts that ones who were drafted later. 

Tracing back to the NFL the contracts that rookies sign when they are first drafted are completely different than the kinds of deals they can sign once their rookie contract is up. For instance, rookie NFL players generally are not paid a lot compared to veteran NFL players because of something known as the “Rookie Pool”. The Rookie Pool is the maximum limit that the league sets on teams to spend their cap/money on rookie contracts. Once their rookie contracts expire, NFL players can sign deals with teams ranging from as much money as they hope to get. The only limit in this case is the salary cap, which is the amount of total money an NFL team has to spend and this depends on revenue the team gets from ticket, merchandise sales, and more, as well as depending on the other contracts that the other players on the team had signed previously. Thus, as a general manager of a football team, it is their job to ensure and allocate enough money to pay their quarterbacks because the salary cap limits how much they can spend per year.

## Description of Data
This study incorporates data of all quarterbacks of the first four years of their NFL career from 2006-2013 in time interval. This is because a rookie contract lasts four years so collecting the total data of a quarterback in a span of those four years was needed. The statistics shown there are all available and from the official NFL website. The total variables that were looked at in this study are as shown below:

![Untitled (2)](https://user-images.githubusercontent.com/54411602/63632478-84f2c580-c5eb-11e9-9f69-8f29f75be7ee.png)

Furthermore, the following table displays the summary statistics of all the variables that were looked at in this study:

![Untitled2 (2)](https://user-images.githubusercontent.com/54411602/63632481-90de8780-c5eb-11e9-986d-c79acfffd759.png)

Because there were numerous quarterbacks drafted into the NFL who did not play a single down or have enough data, they were dropped from the study. The cutoff point was at 30 pass attempts. As a result, the final sample size was 62 QBs, compared to the initial 94.

## Empirical Results
Because of multicollinearity, numerous variables were experimented and included in and out of the regression model, in order to determine what the preferred final model should be. In order to figure this out, on Stata, a correlation between all the independent variables was implemented to ascertain the correlations.

![Untitled3 (2)](https://user-images.githubusercontent.com/54411602/63632490-b7042780-c5eb-11e9-86fb-cef17c3a65a7.png)

As shown above, since PassTDs was the most correlated variable to Future_Salary, it was decided that the final model should at least include that. However, PassTDs was also highly correlated with a plethora of the other independent variables so I was restricted in which other variables I can also include. As a result, PassTDs, Rush_Yards, QBR, and Pro_Bowls were then decided to be in the final model. To add on, because the dataset spanned from 2006-2013, inflation was accounted for as well; plus, it is a given fact that the salary cap in the NFL has steadily increased per year so in order to account for that, dummy variables were created for every year. However, the year dummy variables were not statistically significant; thus, they were left off in the final model. 

The regression results are shown below:

![Untitled4 (2)](https://user-images.githubusercontent.com/54411602/63632494-d0a56f00-c5eb-11e9-8402-93c2adac5fc2.png)

In a statistical standpoint, there is statistical significance between future salary and the four variables as the p-value was .000. Though individually, only PassTDs and QBR are shown to have statistical significance with future salary while Rush_Yards and Pro_Bowls do not. At an economic standpoint, for every passing touchdown a quarterback throws, he gains an additional $151,021, for every single rushing yard gained, he loses an additional $1,563, for every one unit increase in QBR, he earns another $130,795, and for every Pro Bowl entry, he wins another $1,722,651, assuming all other variables are constant for each case. As a result, this is economically significant since the quarterbacks is either earning an additional $100,000 to $1,000,000 ish for every increment increase in the respective variable case in passing touchdowns, QBR, or Pro Bowl. 

## Conclusion
From the results of the multiple regression model, it can be concluded that there was only statistical significance between the future salary of NFL quarterbacks and passing touchdowns and QBR. This would make sense, as more passing touchdowns and a higher QBR would lead to an increase in salary. However, the fact that rushing yards has a negative association with future salary is intriguing. It could be because incompetent quarterbacks tend to run the ball more compared to far superior quarterbacks who can make plays with his arm rather than his feet. Furthermore, there was no statistical significance between future salary and pro bowls. This could be because sports fans are the ones who vote which players should be inducted to the Pro Bowl so the system is flawed. Therefore, Pro Bowls do not indicate how talented a quarterback can be. 

By no means is this a perfect model. For instance, injury is a major factor when it comes to professional sports, but finding data on it is near impossible since injuries is not a variable that is generally accurately recorded by the NFL. 

## References
Buschemann, A. & Deutscher, C. (2016). Does Performance Consistency Pay Off Financially for Players? Evidence From the Bundesliga. Department of Sport Science, 71, (27-43). 	

Tang, M. (2015). Contract Length, Expected Surplus, and Specific Investments. Department of Economics, 16, (295-311). 
