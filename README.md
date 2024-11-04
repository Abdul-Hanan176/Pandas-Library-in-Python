# import Numpy & Pandas Library
import numpy as np
import pandas as pd
# Creating Dictionary
AINT_4A={
    "Name"           :['Abdul_Hanan','Taha_Shehzad','Aamish_Gujjar','Muhammad_Abuzar','Fahad_Mukhtar','Jamil_Bassum','Zahid_Hanif','Ibtasam','Ali_Hassan','Asad_javed'],
    "Registration no": 
          ['DSAI232103032','DSAI232103007','DSAI232103034','DSAI232103009','DSAI232103020','DSAI232103016','DSAI232103003','DSAI232103026','DSAI232103043','DSAI232103032'],
    "Ai_Marks"       :[85,75,65,55,50,52,45,25,35,77],
    "City"           :["Dera Bugti","Rahim Yar khan","D.G khan","Multan","Sadiqabad","Rahim yar khan","Bolan","Rahim Yar Khan","Koi Thikana nhi","R.Y.K"],
    "Attendance"     :['85%','75%','65%','55%','50%','52%','45%','25%','35%','77%'],
    "Grade"          :['A','B','C','D','D','D','F','F','F','B']
}
# DataFrame is equals to the df variable
df=pd.DataFrame(AINT_4A)
# print the DataFrame
df
# Convert DataFrame to csv file
df.to_csv('Assignt.csv')
# Index column equals to Name column
pd.read_csv("Assignt.csv", index_col = "Name")
# Read csv file and the file equals to the Assignt variable
Assignt = pd.read_csv("Assignt.csv", index_col = "Name")
# print top 4 rows
Assignt.head(4)
# print button 4 rows
Assignt.tail(4)
# check length of the csv file
len(Assignt)
# check shape of the csv file
Assignt.shape
# check size
Assignt.size
# check the data types of the csv file
Assignt.dtypes
# check index location
Assignt.iloc[9]
# Search the data in the csv file
Assignt.loc["Abdul_Hanan"]
# sort in ascending form
Assignt.sort_values(by = "Grade", ascending = False).head()
# sort two columns
Assignt.sort_values(by = ["Ai_Marks", "Attendance"]).head()
# sort index and print print top of the rows
Assignt.sort_index().head()
Assignt["Registration no"]
Assignt["Registration no"].value_counts().head(10)
# Add new column 
Assignt['Rank'] = range(1, len(Assignt) + 1)
print(Assignt)
print(Assignt[Assignt['Grade'] == 'Universal'])

