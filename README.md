EDA on the Titanic Dataset
This was one of the tasks from an AI/ML internship I did, and it's exactly what it sounds like — no modeling here, just me digging into the classic Titanic dataset to actually understand it before anyone thinks about building a survival predictor on top of it. If you've done any ML learning path, you've probably run into this dataset a dozen times, but going through the EDA properly is what actually teaches you something.
What I actually did
Got familiar with the data first — loaded it up, checked .info(), .describe(), and .isnull().sum() to see how many records, what types of features, and where the missing values were hiding (Age and Cabin both have gaps).
Looked at the summary stats for numerical and categorical columns to get a feel for typical values, ranges, and skew.
Then got into the visuals: histograms across all numeric columns, a boxplot of Age by Pclass, a pairplot of Age/Fare/Pclass/Survived colored by survival, a correlation heatmap over the numeric columns, and a closer look at Fare's distribution with a KDE overlay plus direct skewness checks.
What stood out

Women survived at noticeably higher rates than men
First class passengers had better survival odds than second or third class
Both Age and Fare are skewed, with some pretty extreme values in Fare especially — something I'd need to deal with before this data goes near a model

None of this is exactly a shocking revelation if you know Titanic history, but the point was to actually derive it from the data instead of just knowing it going in, and to catch the messier stuff that isn't obvious until you look.
Stack: Python, Pandas, Matplotlib, Seaborn
