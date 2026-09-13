# Prediction of the 2026 American Midterm Elections using Data Science, Programming, and Statistics
## Developed by Kyle Truschel

## Abstract
The upcoming 2026 midterm elections in the United States is primed to be one of the most divisive and consequential elections, with many important swing states that will change the power balance of the United States. This project will attempt to predict the senate races for three key swing states of Michigan, Maine, and Georgia and will utilize many of the skills I have developed from the courses during my undergraduate studies in the realm of data science, computer science, and statistics.. The prediction results will be displayed as a website and published on a weekly basis for the current percentage and likelihood for the candidates of the three swing states mentioned. The project will conclude in November with the end of the actual midterm elections, and the results of the project will be concluded and attempt to process the correct predictions and what may have influenced the results. The three main methods of prediction will involve using previous election data, reputable polling data, and volatility index formulas to calculate predictions for candidates. The previous election data will be gathered from the 2024 American midterm elections for Michigan and Maine and the 2022 Georgia midterm election. This initial data will be used as a baseline for further data. The polling data will be gathered on a weekly basis from reputable US polling data research institutions. This data will be used to supplement the initial data. Lastly, a formula will be used to incorporate volatility by comparing voter swing patterns.

## Background
The US midterm elections present an opportunity for American citizens to cast their votes to decide who should be elected to the US Congress, in both the US House of Representatives and the US Senate, in order to represent the ideals and demands of the people. With this responsibility, lawmakers are given the ability to hold and control power over the US Government and decide how to use it for who they represent. Given the current political climate in the United States, the 2026 midterm elections is likely to be a consequential event as it coincides with the divisiveness of the demands of the American people and the elected representatives who are becoming less favorable in the eyes of the American population. Political events such as the American war in Iran, the Israel war in Gaza, the Russian war in Ukraine, climbing inflation, healthcare, climate change, and the economy as a whole has many of the American people dissatisfied with their current representatives in the US Congress. The decision of the US midterms will conclude on November 3rd, and the results not known until days after as votes are recounted and confirmed to maintain integrity. 

Analysis of politics has often been a difficult endeavor due to the nature of predicting elections. Similar to predicting the stock market or weather, much of the data gathered from political events is forecasted and is under review to change as candidate controversy, voter turnout, and corruption within political parties influence the elections. Fortunately, there are many reputable institutions who are tasked with overcoming this endeavor in the field of gathering data from polling from samples of the population to better understand how voters feel about candidates and their policy proposals. With this idea in mind, the entire purpose of this project will be to better understand how the 2026 midterm elections will conclude.

## Methodology
In the US, many states are known as "Blue", "Red", and "Swing States" (or Purple states as a mix of the two colors), where typically blue aligns with the Democrat party and red aligns with the Republican party, and the swing states can result in either party or a third party. According to a study by Cambridge University Press, they mentioned the previously acknowledged challenges of forecasting elections, such as voter turnout being a major issue. Despite this challenge, they affirm the first step of initial analysis must begin with establishing a baseline of a model (Camatarri). With this aforementioned concept in mind, the baseline gathering of data will take the previous election results from a state's last election to get a better understanding on how voters in a particular state will lean.  For instance, the last election in Michigan was 2024 in which the Democrats gained a very slim majority of votes compared to Republican candidates. This indicates that the state falls under the "swing state" category and could have the potential to go to either party. The baseline data will be presented on a bar chart graph that displays the percentage of votes from the Democrat, Republican, and third party candidates.

The second prediction methodology will be taking the most concrete data, which is the current week's most recent voter sentiment in the form of polling data. Reputable polling institutions such as YouGov, Ipsos, Emerson College, and the University of Massachusetts are tasked to conduct surveys and research in order to gather sample sizes of voters on who they plan to vote for on November 3rd. This data will be the most accurate as it confirms voters who will not cast a vote or who are not interested in voting are not conducted in the polling institution's survey. However, this also assumes that the voters who did conduct the survey will actually turnout to vote. Ultimately, this data will be the most accurate representation on how voter behavior will influence the midterm elections. This data will be compiled into a separate bar chart graph to display each candidate's favorability, based on voter sample size. As the weeks continue towards November 3rd, candidates will gain or lose favorability due to primaries, in which only one Democrat or Republican will be represented on the ballot. This will culminate into a single candidate for the Democrat, Republican, and if gathered, a third party. Finally, this data will be combined with the previous baseline bar chart graph to better understand how sample sizes combined with historical data can be used to predict the midterm election.

A third methodology will attempt to perform a backtest analysis of previous polling data compared to actual results. Since the polling data is the most concrete and current information gathered to estimate how voters will behave during the election cycle, it is important to verify if previous polling data shows the same behavior. With this concept, a backtest analysis will be conducted to gather polling information from the last four senate election races to generate a graph to explain the polling data expectations versus the actual result expectations. With this information, the median of the difference between expectation and actual results will be calculated to generate a median error rate that will be integrated into the final election analysis graph. The median will be preferred over an average due to the potential of erratic polling versus actual results behavior, such as in an instance of a third party winning over polling predictions of the Democrat or Republican party.

This methodology will be calculated by taking the sum of the actual results minus the expected results and divided by the actual results. The calculation will be multiplied by 100 to generate a percent error.

$$
    \text{Percent Error} = \frac{|\text{Actual} - \text{Expected}|}{|\text{Expected}|} \times 100\%
$$

The percent error will be calculated for the three senate parties, Democrat, Republican, and Third, and the median will be generated for the last four senate races for each of the previously mentioned parties.

The percent error must be ordered from lowest to highest percent to calculate the median.

For a sorted dataset $x_1, x_2, \dots, x_n$ ...

$$
\text{Median} =
\begin{cases}
x_{\frac{n+1}{2}}, & \text{if } n \text{ is odd} \\[6pt]
\dfrac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2}, & \text{if } n \text{ is even}
\end{cases}
$$

The median will be used to generate a median error rate that will be displayed as the upper and lower bound on the analysis graph.

The previously mentioned methodologies will be utilised in an algorithm to present a prediction graph of the week’s current senate race analysis. The results of this graph will demonstrate the percentage prediction of a political party’s chance of winning the senate race, along with the median error rate displayed as an upper and lower bound percentage, to consider if polling were to be inaccurate.

## Data Overview
As mentioned in the Methodology section, the first two methods will utilize historical and polling data to be compiled into the final prediction graph, and present the most concrete source of analysis for this project.

The historical data as mentioned is from the state’s most recent senate election, for instance the most recent senate election for Michigan was conducted in 2024, where Democrats won by a slim majority. The source of this data is provided by the official State of Michigan’s website, where the data has been archived by election officials. In essence, this data is concrete and cannot be modified, thus making it a legitimate source of information. This is true for each state’s election results, despite any claim of election fraud, as votes are tallied and counted multiple times even after the conclusion of a senate race.

The polling data serves as the main indicator for voter behavior during a senate race. Pollsters are professionals who are tasked by reputable institutions such as Pew Research Center, YouGov, FiveThirtyEight, and Emerson College to conduct short form interviews and surveys on a state’s district to gather voter indication on which candidates they favor. As the weeks progress towards the end date of the senate race, candidates will be chosen based on certain criteria such as ranked-choice voting and primary elections. The first criteria involves elimination rounds until only one candidate is elected to represent a party. The second criteria is similar, but involves an election a few weeks before the actual general election in which only one candidate is elected to represent a party. This idea is important to consider as candidates who are favored may drop out, be mired in controversy, or lose their primary and ranked choice voting race - all of which influence voter behavior. This behavior will naturally adjust the sample sizes as voters change their minds on candidates.

In addition to using historical data and polling data, a consideration will be used to account for the discrepancy of precision for the percentage amounts. The assumption with combining the percentages skews the precision for the amount of votes received. The historical results have a vote size in the millions compared to current poll size in the thousands or hundred thousands, thus presenting a situation where the data is skewed. According to FiveThirtyEight, the approach of weighting fundamentals compared to current polling should be considered as they state, ”Theoretically, each predictor gets a weight that is inversely proportional to its variance, and you'd end up with a combined median prediction that is closer to the polls (in this example, Trump+3.9) — since they have less uncertainty than the fundamentals (in this example, Biden+1) — and uncertainty that is less than either predictor's uncertainty on its own. Specifically, in this example, the polls should have received about 74 percent of the weight for the final prediction, while the fundamentals should have received 26 percent.” (ABC News) Using this consideration, the polling data will receive a more favorable weighting compared to the historical data with a 70/30 split of the total percentage amount.

The third methodology will utilize a median error rate and be displayed as an upper and lower bound based on the previous methodology percentages, from historical and polling data. This data is gathered from the last four election cycle’s polling versus actual results.

An important consideration for US elections is that voters ultimately may still decide to choose any candidate they desire, even those who are no longer officially running, those who are not eligible to run, and those who are running simply as a joke. This data is ultimately gathered by pollsters but represents an infinitesimal small minority that will not influence an election, but nonetheless is important to consider as this portion of the data is not accurate.

## Programming Overview
This project will use Python, HTML, CSS, and Jupyter Book to compile and display the results of the 2026 senate race.

Jupyter Book provides an opportunity to demonstrate my ability to utilize a new concept with skills I developed in my Research and Writing in CS and Math course. In essence, it excels in the field of Data Science as it creates an organized and formatted webpage to display graphs and data results.

Jupyter Book utilizes the Python library, pandas, to read and sort data from .csv files that can be manipulated to display relevant and important information.

The Python library, matplotlib, will be used to generate each week’s graph which is then saved in order to record the prediction analysis over the course of the senate race. This will be used for analysis of the final results to generate a conclusion of the project.

I intentionally wanted to avoid using an AI algorithm to influence and compile the prediction results, as I believe it introduces a "black box" scenario in which I do not believe the data and methodologies used to produce any result can be verified. AI and Visual Studio Code plugins may be used in the creation of this project to fix common errors and overcome programming obstacles, but it will not be relied upon.

## Results
The results of this project will conclude on November 3rd as will the 2026 senate race. Typically, the senate race will be confirmed a few days after the official end date due to vote tallying and final counting begins by election clerks, who are responsible for verifying the election results.

In addition, this section will attempt to address any possible outliers and correct or incorrect predictions as outlined by the goals of this project. As stated, predicting elections is a difficult endeavor due to the nature of elections, similar to the stock market and weather. Ultimately, this project will provide a general idea of how voters behave especially due to the volatile political climate in the United States.

## Table of Contents

```{tableofcontents}
```

## Working Bilbiography
```{bibliography} references.bib
:all:
```