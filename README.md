![UMBC logo](https://github.com/SAI-GOPAL/Predicting-Future-NFL-Player-Performance-and-Team-Success/assets/46624385/327bfb1a-f4bf-4bf1-b31c-97705ade7f92)       				
![Football image 1](https://github.com/SAI-GOPAL/Predicting-Future-NFL-Player-Performance-and-Team-Success/assets/46624385/75ada9dd-ba47-4aae-9656-0231bdba724e)




# Predicting Future NFL Player Performance and Team Success
**A Data-Driven Study in Fantasy Football**  

**DATA 606 Group 1**  
*David Weir*  
*Balakrishna Bhoomani*  
*Sai Gopal Medisetti*  

*5/10/2024*  
*UMBC*

## Folder Contents

Inside this folder, the user will find the notebooks necessary to replicate (and build upon if they so choose) the *Predicting Future NFL Player Performance and Team Success* study conducted during the Spring 2024 semester. The study produced two deliverables: an annotated Google Colab notebook and a final presentation brief-out. 

Opening the Notebook will allow users to dive into the same datasets and utilize the same regression models our team used to conduct our study. Exploring the final brief-out will give the user context to the results our team was able to garner over the course of the Spring 24 Semester, as well as highlight some next steps that an interested user might pursue.

What follows below is the abstract and original research proposal to give the user full context into the team’s thought process and guiding goals as the project progressed.

# Abstract

One of the quickest-growing markets in the United States is sports betting. By 2024, online sports betting is predicted to bring in $9.65 billion and is growing by 13% year over year ([Statista](https://www.statista.com)). As the legalization of sports betting continues to spread, state by state, the population base for this market keeps on growing. The NFL, as the most popular sport in America, is the likely target of a significant portion of the attention of this market opportunity. One of the most popular ways to bet on the NFL is through fantasy football, a game that uses statistics from real NFL games and allows laypeople to assemble handpicked teams of the best players from across the NFL to compete for them on the virtual gridiron. The big question every fantasy football manager wishes that they had the answer to is this: How do they know who to pick or how a given player will perform relative to his peers in the upcoming season? This paper aims to answer exactly that question, using data collected from as far back as the 2003 season; this research project will examine the top 200 performing players from each season, identify trends, and establish patterns to predict which players will perform better in the next NFL season of play according to both traditional and points per reception scoring models. The traditional fantasy football scoring model awards 1 point for 25 passing yards, 4 points for a passing touchdown, -1 points for an interception, 1 point for 10 receiving or rushing yards, 6 points for a rushing or receiving touchdown, and -1 points for a fumble lost. Additionally, the point-per-reception format awards 1 point for each reception a receiver catches. Furthermore, this study will group the highest-performing players by their teams to predict the overall success of their teams over the course of a given season. Specifically, the hypothesis surrounding this paper is that by analyzing the passing, rushing, or receiving yards and touchdowns a player scores over the course of a given season, and comparing it with previous season data, that the future performance or success of a player can be predicted with at least 60-70% accuracy. That accuracy takes into consideration outliers in the data, as well as the capability for injuries to derail a player’s season. Due to the inherent violence of the sport and the physical explosivity showcased on the field during NFL games, it is not uncommon for NFL players to get injured and miss one or more games during a given season. This project will use alternate methods of regression models, variable correlations, as well as predictive analyses to test the stated hypothesis in an attempt to solve the stated research question.

![image](https://github.com/SAI-GOPAL/Predicting-Future-NFL-Player-Performance-and-Team-Success/assets/46624385/b8ce30b6-bac9-42d5-8e59-7807cb148d0c)

# Introduction

A new frontier—the world of fantasy football—emerges under the bright lights of the NFL as the sun sets on the American sports scene. Imagine a future in which casual fans and armchair quarterbacks become master strategists, building dream teams out of National Football League gridiron gladiators. The NFL offers a wealth of opportunities and interest, especially with online sports betting expected to soar to an astounding $9.65 billion by 2024. Predicting player performance and team success is crucial in this dynamic arena. This study sets out on a data-driven expedition, exploring two crucial questions: Can the NFL's future stars be accurately predicted, and can a player's individual genius predict the destiny of his team as a whole? The combination of tradition and creativity as we venture into this unexplored area offers an exciting trip through the nuances of fantasy football.

# Background

Research on forecasting NFL player performance and team performance in fantasy football has been dynamic, with multiple research adding to the growing body of knowledge in sports analytics. Among the most notable of these is the research conducted by Caleb Panikulam at Arizona State University, which used a TensorFlow Keras AI regression model to predict player-point outcomes. This innovative approach served as the basis for the linear regression methodology used in our study. At the same time, a graduate student at Aalto University took a different approach to the problem of using machine learning to predict NFL game outcomes. Furthermore, Universidad del Rosario research expanded the range of data-driven methodologies by exploring the subtleties of special teams. The study conducted by the University of Central Florida used Decision Trees and XGBoost to analyze wide receivers and offensive lines, deepening our knowledge of player dynamics. The panorama is further enhanced by Winthrop University's investigation into the relationship between AI, the NFL, and Amazon Web Services, as well as by MIT's study that projects defensive players' careers. As we begin this research, we take inspiration from these many studies in an effort to decipher the nuances of forecasting not only the individual player success but also the team success of NFL teams in the fascinating domain of fantasy football.

# Summary of Literature Review

As a result of searching for previous studies with similar objectives or problem statements, several such studies were identified, and six are highlighted in this literature review. The first study highlighted here, conducted by Caleb Panikulam at Arizona State University, is the study that most closely resembles the intention of this study. Similar to this study, Caleb set out to predict an NFL player’s fantasy football points in a given season. Unlike this study, a tensorflow keras AI regression model was used, whereas this study will utilize a linear regression model and has the added complexity of using combined players to predict a team’s success.
The second study identified was conducted by an Aalto University graduate candidate and focused on predicting the results of NFL games using machine learning. This study used logistic regression and random forest algorithm to analyze data from Pro Football Focus’ website. It will be interesting to note the differences in outcomes between this project and the project this paper focuses on, particularly related to the prediction of an overall season’s worth of games played.
The third study researched was conducted by a graduate student from Universidad del Rosario and focused on the special teams aspect of the NFL game particularly. While special teams data is outside of the given scope for this project, there are still lessons to be learned from the data-driven approach used here.
The fourth study identified was conducted by a graduate student at the University of Central Florida and focused on the use of sports analytics in the NFL. This study used machine learning techniques like XGBoost and Decision Trees to analyze wide receiver and offensive line on-field and combine data.
The fifth study considered in the research for this project was conducted by graduate students at Winthrop University and focused on AI’s impact on the NFL from more of a peripheral standpoint. Their study explored the connection between Amazon Web Services, the NFL, and fantasy football.
The sixth study researched was conducted by students at MIT and published by Amazon Science. The study focused on predicting and projecting the careers of defensive players based on observed and recorded player metrics.
After digesting the information contained in these studies and learning from the past methods used and angles of observation previously utilized in the field, our team is ready to present, hypothesize, and answer our own research question in this blossoming field.

# Research Questions

In our study, we aim to leverage data collected from the past two decades of fantasy football to address two primary research questions:
1. **Player Performance Prediction:** Can we accurately predict which NFL players are likely to be the top performers in the upcoming season, considering both traditional and points-per-reception formats? To achieve this, we will analyze statistical trends and patterns among the top 200 performing players from previous seasons, focusing on metrics such as passing, rushing, and receiving yards, as well as touchdowns. By employing regression models, variable correlations, and predictive analyses, we aim to achieve a predictive accuracy of at least 60-70%.
2. **Team Success Prediction:** Additionally, by grouping players by their respective teams, can we utilize their fantasy football statistics to forecast their team's performance in a given season? We will explore correlations between individual player performance and team success, aiming to develop predictive models that can anticipate a team's record based on the aggregated performance of its players.
Our approach will involve thorough data analysis, employing advanced statistical techniques to identify significant trends and relationships within the fantasy football dataset. By drawing on our expertise in data analytics and predictive modeling, we are confident in our ability to provide valuable insights into player and team performance dynamics in the NFL, ultimately aiding fantasy football managers in making informed decisions for their teams.

# Preliminary Implications

As established above, the sports betting industry is growing rapidly, especially as more and more States legalize sports gambling. This highlights the need for more studies to be done into sports betting to examine the efficacy and further assist in educating the population about how they can best enjoy this new entertainment avenue. The patterns, trends, and analyses established in this paper can greatly affect strategies used by new and seasoned fantasy football managers alike, as managers are constantly trying to establish a competitive edge over one another.
This project will build on top of existing projects like those mentioned above from Arizona State and Aalto University to not only help predict individual fantasy football player success but also take a new approach to predicting team success. Given that the scoring methods for traditional football and fantasy football are inherently different, combining the two scoring standards has seldom been done. This project aims to do exactly that in an attempt to establish new patterns and trends for predicting a team’s on-field performance.

# Conclusions

The proposal aims to leverage past fantasy football data to predict player and team performance in upcoming NFL seasons. By analyzing trends and employing regression models, the study seeks to achieve predictive accuracy of 60-70%. Drawing on previous research and employing advanced statistical techniques, the study hopes to provide valuable insights for fantasy football managers and contribute to the growing sports betting industry. This innovative approach combines traditional and points-per-reception scoring models to predict team success, offering a unique perspective in the field. Overall, the study addresses a significant gap in research and aims to provide actionable insights for both novice and experienced fantasy football managers.
![image](https://github.com/SAI-GOPAL/Predicting-Future-NFL-Player-Performance-and-Team-Success/assets/46624385/909c3a9d-77c2-4a4a-bdfb-216d105a7b81)
![image](https://github.com/SAI-GOPAL/Predicting-Future-NFL-Player-Performance-and-Team-Success/assets/46624385/44e4c348-5d3d-4d69-a72c-519507319a3f)


# References

**Works Cited**
- Barbarosa, Santiago. Enhancing Performance in Special Teams within the NFL through Reinforcement Learning: A Data-Driven Approach. 17 Aug. 2023, [Repository](https://repository.urosario.edu.co/server/api/core/bitstreams/5e326c11-4d05-4982-8ade-80f76 f66a8d7/content). Accessed 10 Mar. 2024.
- Garrett, Jared. Examining the Impact of Artificial Intelligence in the NFL amongst College Students. 4 Dec. 2019, [Digital Commons](https://digitalcommons.winthrop.edu/source/SOURCE_2019/posterpresentations/61/). Accessed 10 Mar. 2024.
- Juuri, Sebastian. Predicting the Results of NFL Games Using Machine Learning. 1 Jan. 2023, [Aalto Doc](https://aaltodoc.aalto.fi/items/8a329777-bdfe-4800-8d8d-d6dc3e75be70). Accessed 10 Mar. 2024.
- “Online Sports Betting - US | Statista Market Forecast.” Statista. 1 Jan. 2024, [Statista](https://www.statista.com/outlook/dmo/eservices/online-gambling/online-sports-betting/united-states#:~:text=The%20Online%20Sports%20Betting%20market). Accessed 10 Mar. 2024.
- Panikulam, Caleb. Predict NFL Players Points for Fantasy Football. 1 Dec. 2022, [Keep Lib](https://keep.lib.asu.edu/items/170262). Accessed 10 Mar. 2024.
- “Prediction of Defensive Player Trajectories in NFL Games with Defender CNN-LSTM Model.” Amazon Science. 1 Jan. 2021, [Amazon Science](https://www.amazon.science/publications/prediction-of-defensive-player-trajectories-in-nfl-games-with-defender-cnn-lstm-model). Accessed 10 Mar. 2024.
- Schoberg, Christopher. Football by the Numbers: A Look into Sports Analytics Currently Used in the National Football League. 1 Aug. 2023, [Stars Library](https://stars.library.ucf.edu/etd2020/1762/). Accessed 10 Mar. 2024.
