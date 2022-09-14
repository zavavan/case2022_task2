# Task 2 - Automatically replicating manually created datasets of COVID-related protest events

The goal of this task is to evaluate the performance of automatic event detection systems on modeling the spatial and temporal pattern of social protest movements related to the various aspects of COVID pandemic. Namely, the participants will have the possibility to evaluate their systems on reproducing a manually curated
dataset of COVID-related protests in the US spanning three months (July 27, 2020 through October 27, 2020). This is an high-level task that implies detection and  deduplication of protest event reports, enriched with location and date attributes. 
The event definition applied for coding the reference event dataset is the same as the one adopted for Task 1. No additional training data will be provided for this task, however participants may utilize any other data source to improve performance of their submission. 
The participant systems will be evaluated on three input data collections:
  - an English language news corpus comprising a large selection of COVID-related news sources from the US
  - an English language tweet collection comprising daily samples of COVID-related tweets with some geographical metadata referring to U.S.
  - a Spanish language tweet collection comprising daily samples of COVID-related tweets with some geographical metadata referring to U.S.
  - 
All sources contains data from July 27, 2020 through October 27, 2020. The details of obtaining the data from its source are provided in the folders news and twitter.

The evaluation will be performed on a manually curated list of COVID.-related protests events from ACLED () for the relevant period. You may either process a data source you choose or both. Please submit separate files for the events you extracted from the source(s) you choose. If you want to combine/merge/integrate the results from each source in a file, you can create a third file. 

The full description of the task is available in this <a href="https://github.com/zavavan/case2022_task2/blob/a2a8dd5b51cfc6951b288bed3c919e6b7051cfc4/Task2_Description.pdf">file</a> and a sample submission format can be found in this <a href="https://github.com/zavavan/case2022_task2/blob/56b1ac3560f89548cf6876d2d871f00683a6730f/submission.myteam.news.3.csv">file</a>.

Please send the submission files to ahurriyetoglu@gmail.com, hristo.tanev@ec.europa.eu. For further details please contact Vanni Zavarella (vanzavavan@gmail.com)
