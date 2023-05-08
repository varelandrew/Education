# Is School Performance Predicted By Socioeconomic Factors?

# Description
- The purpose of the project is to answer the question of whether school performance can be predicted by socioeconomic factors, and answer my additional proposal of whether State's can predict school performance or socioeconomic factors.I will be using python to perform operations that help me towards answering the above question. This includes cleaning up the provided data, and creating regression models to analyze how well variables can predict the average ACT score.
- General conclusions that I discovered from performing the above methods consist of creating multiple linear regression models and discovering the best subset of predictors which are rate of unemployment, percent of students that are going to attend college, and percent of students that require free/reduced lunch. Where percent of students that require free/reduced lunch is found to be the best predictor for finding a school's average ACT performance. Adding a categorical predictor like State's also showed being a good predictor for a school's average ACT performance, but not a good predictor for socioeconomic factors. A more in depth conclusion can be viewed at [Communication Presentation](https://github.com/varelandrew/Education/blob/main/CommunicateTheResultsEducation.pptx) and [Analysis Notebook](https://github.com/varelandrew/Education/blob/main/Andrew_Varela_DATA_3320_Education_Analysis.ipynb).

# Requirements
- In order to complete this project I had the help from a few tools. I used Google Colab as a notebook for my code to perform my desired actions when it came to answering the question of this project. Python was my programming language of choice as it has many libraries that make plotting and cleaning up data easy. Finally, I used GitHub as my project storage as it makes it easy to link and store files that I used and created for this project.

# Data
- This project utilizes two data sets [Edgap Data Set](https://github.com/varelandrew/Education/blob/main/EdGap_data.xlsx) and [NCES Data Set](https://www.dropbox.com/s/lkl5nvcdmwyoban/ccd_sch_029_1617_w_1a_11212017.csv?dl=0). The primary data set is the EdGap data set from [Edgap](https://www.edgap.org/#5/37.875/-96.987). This data set from 2016 includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district. The secondary data set is basic information about each school from [NCES](https://nces.ed.gov/ccd/pubschuniv.asp).

# Data Preparation
- What steps did I take to prepare a cleaned up version of the data sets from the websites above?
  1. I first imported necessary libraries and loaded the two data sets.
  2. I then explored the data sets to see what I was working with and what needed to be cleaned up.
  3. First thing I noticed was that both data sets had a NCESSCH column, but one was a float type and the other was a int type. So I converted the float type to an int type.
  4. I then changed the school_info data set to only have relevant data that I would use as there was a lot of data that would've been unused.
  5. Once the school_info data set was changed I ended up renaming all of the columns in both edgap and school_info to be lowercase, snake_case, readable, and ready to be merged.
  6. I merged the two data frames into a new one that contained all of the values from edgap and school_info on edgaps id column.
  7. I proceeded to tidy up the data set by fixing values that were incorrect like negative percentages or less than 1 for an average act score, as well as removing other school levels as high school felt like the whole relevant level for me to answer the question.
  8. Next step was to perform a train test split on the data set to predict average_act scores. I did this by splitting the data into training and testing sets, where I am keeping 20% of the data for the test set.
  9. I then imputed the data to replace missing values in the columns corresponding to predictor variables in the anaylsis by using all numeric values other than average_act score.
  10. Lastly, I joined the x_train and y_train data sets together to make the clean data set easy to plot and visualize.
  11. Then I exported the clean data set.
  
 Here you can find the python file that follows these steps I listed: [Data Preparation File](https://github.com/varelandrew/Education/blob/main/Andrew_Varela_DATA_3320_Education_Inequality_Data_Preparation_Template.ipynb)
 
 Here you can find the cleaned csv file: [Clean Data](https://github.com/varelandrew/Education/blob/main/clean_education.csv)

# Authors
- The author of this project is Andrew Varela, a 4th year Computer Science major with a minor in Data Science currently attending Seattle University. You can find Andrew Varela on [Linkedin](https://www.linkedin.com/in/andrew-varela-a827a71b6/)

# License
- The owner of this project grants permission to use information from this repository.
