# Is School Performance Predicted By Socioeconomic Factors?

# What Is The Purpose Of The Project?
- This project addresses inequality of educational opportunity in U.S. high schools. We want to utilize the data to see if school performance can be predicted by socioeconomic factors. Using the data provided below we can compare ACT and SAT scores for schools with socioeconomic characteristics to basic information about each school to dictate whether socioeconomic factors affect school performance.  

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
  8. I then exported the data into a csv file.
  
 Here you can find the python file that follows these steps I listed: [Data Preparation File](https://github.com/varelandrew/Education/blob/main/Andrew_Varela_DATA_3320_Education_Inequality_Data_Preparation_Template.ipynb)
 
 Here you can find the cleaned csv file: [Clean Data](https://github.com/varelandrew/Education/blob/main/clean_education.csv)
