Movies Data 
------
The original data comes from IMDb movie, which is the most popular movie website, and it includes each movie's information such as movie plot description, Metastore ratings, reviews, release dates, and many more aspects. The full dataset can be access [this link](https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+movies.csv)

Format of the data
------
Out of all variables from the movies dataset, we used description and genre columns. We built a multi-label classification model that detects different genres of movies, which predicts a probability of each genre for each movie. We used movie descriptions as our input feature and genres as the class label outputs (20 genres).  
5 of genres were dropped because each of their contribution is less than 1% of the class label. Our dataset has 20 class label outputs for each movie (each class will have 0 or 1 - e.g. present or not present) and 1 column for movie description. 

Train/Dev/Test split 
------
After preprocessing the data, we split the movies into Train/Dev/Test (80%/10%/10%). 
Data| Shape|
| ------ |:---:|
Train | 66455 rows, 21 columns |
Dev | 8307 rows, 21 columns |
Test | 8307 rows, 1 columns |
Test_Gold_Label | 8307 rows, 1 columns |


Example of the data 
------

#### Train 

Action| Adventure| Animation| Biography| Comedy| Crime| Drama| Family| Fantasy| History| Horror| Music| Musical| Mystery| Romance| Sci-Fi| Sport| Thriller| War| Western| description
| ------------- |:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|
0|0|0|0|1|0|0|0|0|0|0|0|0|0|1|0|0|0|0|0|julie  successful magazine columnist opens pandoras box  seeks   anonymous sperm donor  fathered  young son
1|1|0|0|0|1|0|0|0|0|0|0|0|0|0|0|0|0|0|0| arizona frank slaytons gang robs  stagecoach  kidnaps ben warrens fianc e prompting warren  pursue slayton



#### Dev 

Action| Adventure| Animation| Biography| Comedy| Crime| Drama| Family| Fantasy| History| Horror| Music| Musical| Mystery| Romance| Sci-Fi| Sport| Thriller| War| Western| description
| ------------- |:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|
0|0|0|0|0|0|1|1|0|0|0|0|0|0|0|0|0|0|0|0| story starts   childish play   brother  sister  continues  huge developments  passing  many difficult barriers  lovely children reach  peak  perfection niaz grows like  grain  blossoms
0|0|0|0|1|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0| marketing department   pharmaceutical company decides  find  dentist  endorse  brand  toothpaste


#### Test 
| description  |
| ------------- |
| high school basketball coach dinah groshardt falls   school secretary carly lumpkin  upsets  entire school   process |
| greedy sailors capture  giant lizard   coast  ireland  sell    london circus   mother shows up  |

#### Test Gold Label 
Action| Adventure| Animation| Biography| Comedy| Crime| Drama| Family| Fantasy| History| Horror| Music| Musical| Mystery| Romance| Sci-Fi| Sport| Thriller| War| Western
| ------------- |:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:| -----:|:-------------:|
0|0|0|0|1|0|1|0|0|0|0|0|0|0|1|0|0|0|0|0
0|0|0|0|0|0|0|0|0|0|1|0|0|0|0|1|0|0|0|0





