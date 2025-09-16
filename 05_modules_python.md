# PANDAS
- library used for data manipulation or handling data in tabular format such as excel file or a csv file etc.
- import pandas as pd

  # dataseries
  - two types of data in this library : 1D which is data series similar to array and 2D is data frame.
  - DATA SERIES
  - pd.Series(["tanmay","rudraksh","riya","priya"])
  - changing index in data series: s2=pd.Series([200,400,500,700,800],index=["stu1","stu2","stu3","stu4","stu5"])
  - slicing : pd.Series["stu2":stu4"] #string upper range index is inclusive but if numeric index then upper range is exclusive
  - updating element in data series : s2[2]=330
  - adding elemnts in data series: s2.append and s2.insert will throw error so right way is s2[new index]=new element i.e. s2[5]=900
  - deleting elements from series: s2.drop(3)
  - merging the series use concat : a=pd.Series([23,4,5,3,432,4,5,6,4,5,3])   b=pd.Series([3,24,52,32,42,24,35,26,24,25,23])  pd.concat([a,b]) #gives individual indexes to series
  - if pd.concat([a,b] , ignore_index=True) will not give individual indexes to series

  # dataframe
  - pd.DataFrame([["Tanmay",45,"male"],["Aakash",21,"male"],["Gyatri",22,"female"]],columns=["Name","Age","Gender"])
    -> output will be i form of table havin columns name age gender
    -> Name	Age	Gender
      0	Tanmay	45	male
      1	Aakash	21	male
      2	Gyatri	22	female
    -> np.array([["Tanmay",45,"male"],["Aakash",21,"male"],["Gyatri",22,"female"]]) if we run it as array we will get a matrix
  - you can crete a dataframe from dictionary
      -> d={"Name":["Tanmay","Aakash","Gayatri"],"Age":[45,21,22],"Gender":["male","male","female"]}
      df=pd.DataFrame(d)
      df
  - for retrieveing values we use loc and iloc in dataframe
      df.loc[2]
      -> Name      Gayatri
          Age            22
          Gender     female
          salary      50000
      df.loc[2,'Gender']
      -> female
      df.loc[2:3,"Age":"Gender"]
      -> Age	Gender
        2	22	female
        3	23	male
  - now you cant use iloc like this i.e. index location it only takes numeric column not like loc
      df.iloc[4:6,2:4]
      -> Gender	salary
          4	male	23000
          5	male	70000
  - concat is used similarly and you can add a new column easily dataframe["column_name"]=values
  - can do something like this also: new_df["Total"]=new_df["English"]+new_df["Maths"]+new_df["Science"]
  - deleting using drop function by default axis is 0 which is for rows and axis 1 is for column
 
    # working in a csv file
    - cars_df=pd.read_csv(r"C:\Users\hp\PYTHON ML\cars.csv")  # here r means to read the file and csv means comma seprated file ,if file is excel then we use read_excel()
    - to get unique values : cars_df["brand"].unique()
    - to get count of unique values: cars_df["brand"].nunique()
    - give count of the elemtns in that row: cars_df["brand"].value_counts()

    # pandas data filter
    - filter us based cars where milege is above 30
      ->f1=cars_df["brand"]==" US." #filter 1
        f2=cars_df["mpg"]>30 #filter 2
        cars_df[f1 & f2]
    - writing in another format: cars_df[(cars_df["brand"]==" Japan.") & (cars_df["mpg"]>20) & (cars_df["hp"]>100)]
    - missing values in each column: cars_df.isnull().sum()
    - checking the duplicate record: cars_df.duplicated().sum()
    - we have nulls we can either drop them(df.dropna(inplace=True)) or we replace them(df.fillna(inplace=True)) with mean/median/mode
    - in case if we have duplicate records, we have to ultimately drop them: df.drop_duplicates(inplace=True)
    - Removing the unwanted columns: df.drop("Unnamed: 0",axis=1,inplace=True)

    # visualization
    - USE MATPLOT WHEN YOU NEED TO CREATE bar plots, scatter plots, line plots, or histograms .  low-level library allowing you to customize individual elements like axes, labels, legends, colors, and line styles with great precision
    - USE SEABORN WHEN statistical visualizations, offering built-in functions for heatmaps, violin plots, box plots, joint plots, and more, often requiring less code than Matplotlib for these types of plots
    - import matplotlib.pyplot as plt
    - import seaborn as sns
    - customization of plot
- figure helps to resize the plot making it larger or smaller
- figsize has length and breadth as parameter 
plt.figure(figsize=(10,2))
plt.plot(x,y)
plt.show()
- to make bar plot: plt.bar(x,y)
- other example and giving labels
age=[10,11,12,13,14,16,18]
height=[100,110,120,130,132,150,170]
plt.figure(figsize=(10,5))
plt.xlabel("Age of students")
plt.ylabel("Height of students")
plt.plot(age,height,color="pink")#changing color of plot
plt.show()
- customizing the values in x axis and y axis
students=["Tanmay",'chakri',"aditya","Vinay","Abhishek","Deekshit"]
score=[80,89,92,78,95,91]
plt.figure(figsize=(2,2))
plt.xlabel("names of students")
plt.ylabel("score of students")
plt.xticks(rotation=60,color="Green") #helps to rotate the x label so that do not overlap cn be seen clearly
plt.yticks(rotation=90,color="red") #rotate ylbel 
plt.plot(students,score,color="pink")
plt.show() #to see the output of plots
- to give title to plot use ply.title()

- SOMETIMES WE ARE WROKING WITH A DATASET THAT GIVES VERY SCATTERED PLOT SO IT IS OKAY TO GROUP THE DATA AND THEN MAKE A PLOT
- so we group this data  , but if we take sns then it btdefault takes the mean 
    ->x=cars_df.groupby("brand")["mpg"].mean() #meaning taking average of values to see clearly 
    ->plt.plot(x)
- sometimes with plt.plot it os dfficult to drw insight so we use sns
- this shaded region is the ocnfidence level or interval
      sns.lineplot(data=cars_df,x="brand",y="mpg")
      plt.xlabel("brand")
      plt.ylabel("mpg")
      plt.title("brand vs mpg")
      plt.show()
- making bar plot in matplotlib : plt.bar(cars_df["hp"],cars_df["mpg"])    ->  usually bar plot is prefered for categorical variables in the x axis
  -> for horizontal barplot use barh
- making bar plot in sns : sns.barplot(data=cars_df,x="hp",y="mpg")
- scatterplot - observe the trends as well as density : plt.scatter(cars_df["mpg"],cars_df["hp"],color="red")
- we can change the shape of our marker s means square : plt.scatter(cars_df["mpg"],cars_df["hp"],color="red",marker="s")
- hisogram - use to compare the distribution of numerical columns , takes only variable for analysis , Bins are used in histograms to group data into ranges of values, means between the bars gap is 10 if we want bigger range then suppose we give 20 the it will have gap of 20
      -> plt.hist(cars_df["hp"],bins=10)
      -> sns.histplot(data=cars_df,x="hp")
- boxplot - used for comparing distribution of numerical continuos values and for statistical analysis or outlier analysis
plt.boxplot(cars_df["hp"])
- pie chart is only available in matplotlib
  -> cars_count=cars_df["brand"].value_counts().values
      country=cars_df["brand"].value_counts().index
      #autopct means their percentage count should also be there
      plt.pie(cars_count,labels=country,autopct="%.5f%%")
      plt.show()
- countplot - only available in seaborn
    -> sns.countplot(data=cars_df,x="brand")
- distributuion plot can be alternative to hist plot
  -> sns.displot(data=cars_df,x="mpg",kind="kde") # KDE- Kernel Density Estimator , #KDE gives only the curve
- heatmap -whebver we need to visualize our data in form of matrix
  -> sns.heatmap(A,cmap="Blues",annot=True,fmt="d")
      #cmap means color like here blues means shade of blue you can give greens
      #annot =True will give annotations to our map
      #fmt means format here dmeans decimal

- cor() gives us a relationship between two variables and can be done only for numerical columns...to get correlation matrix we use: cars_df.corr(numeric_only=True)
- can make a heatmao using this

- seaborn has special paramrter known as hue
- it is kinda similar to labels

# subplot
- creating multiple olot in single plot
- suppose you want to create line plot for hp
- and barplot for hpg and cylinder
- now you want to plot in single space consider like a matrix
- you can either have 2 plots in same row or same column i.e. 2*1 or 1*2
- if we would have 4 graphs then ur matrix would be 2*2 
- thats why we use 2,1 you can use 1,2 also

  >plt.subplots(1,2,figsize=(10,10))
    plt.subplot(1,2,1) #means in our 1 ,2 shape our 1 will be lineplot 
    plt.plot(cars_df["hp"])
    plt.xlabel("trend if hp")
    plt.subplot(1,2,2) #2md would be barplot
    plt.bar(cars_df["cylinders"],cars_df["mpg"])
    plt.xlabel("cylinders")
    plt.ylabel("mpg")
    plt.show()

-seaborn.pairplot() method is used for visualizing relationships between multiple variables in a dataset. By creating a grid of scatter plots it helps to identify how different features interact with each other to identify patterns, correlations and trends in data.
- sns.pairplot(cars_df,hue="brand")

# astype
- astype can be used in dataframe to change the type of you data
- df["column_name"]=df["column_name"].astype(int)
- but if there are some things that astype cant covert to int it will throw error
- so do this
- df["coumnname"]=pd.to_numeric(df["columnname"],errors="ignore")
- errors can have raise (default) or coerce (meaning converting them to null values)
