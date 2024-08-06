# project-01-MJJS

#Jordan's Code Segments
#Grabbing our values of Certificate, Rating, & Metascore
rating_scores = clean_movie_data[["Certificate", "Rating", "Metascore"]]
rating_scores

#Converting to a dataframe
movie_data_df = pd.DataFrame(rating_scores)

#Calculating our average based on Cerificate Rating
average_rating = movie_data_df.groupby('Certificate')['Rating'].mean().reset_index()
average_rating_df = average_rating
average_rating_df

#Converting to a dataframe
movie_data_df = pd.DataFrame(rating_scores)

#Calculating our average based on Cerificate Rating
average_rating = movie_data_df.groupby('Certificate')['Rating'].mean().reset_index()
average_rating_df = average_rating
average_rating_df

#Creating our Visualization and Graphs
#Bar Graph Version
#Creating our x axis and our Tick locations
x_axis= np.arange(len(average_metascore_df))
tick_locations = [value + 0.4 for value in x_axis]

#Creating the figure
plt.figure(figsize=(25,6))
plt.bar(x_axis, average_metascore_df['Metascore'], color = "Purple", alpha = 0.5, align = "center")

#Creating our labels
plt.title("Average Metascore by Certificate")
plt.xlabel("Certificate")
plt.ylabel("Average Metascore")
plt.grid()

# Setting the x-axis labels
plt.xticks(ticks=x_axis, labels=average_metascore_df['Certificate'])

#Saving as a JPG
plt.savefig('metascore_average_graph.jpg', format='jpeg')

#Bar Graph Version
#Creating our x axis and our Tick locations
x_axis= np.arange(len(average_rating_df))
tick_locations = [value + 0.4 for value in x_axis]

#Creating the figure
plt.figure(figsize=(25,6))
plt.bar(x_axis, average_rating_df['Rating'], color = "Green", alpha = 0.5, align = "center")

#Creating our labels
plt.title("Average IMDB Ratings by Certificate")
plt.xlabel("Certificate")
plt.ylabel("Average Rating")
plt.grid()

# Setting the x-axis labels
plt.xticks(ticks=x_axis, labels=average_rating_df['Certificate'])

#Saving as a JPG
plt.savefig('rating_average_graph.jpg', format='jpeg')

#Scatter Plot Version Rating
x_axis = movie_data_df["Certificate"]
y_axis = movie_data_df["Rating"]

#Creating the figure size for Bargraph
plt.figure(figsize=(20,10))
plt.scatter(x_axis, y_axis, marker = "o", color = "green")
plt.xlabel("Certificate")
plt.ylabel("Average Rating")
plt.grid()
plt.title("IMDB Rating scores by certificate")

#Saving as a JPG
plt.savefig('rating_scatter_graph.jpg', format='jpeg')

#Scatter Plot Version Rating
x_axis = movie_data_df["Certificate"]
y_axis = movie_data_df["Rating"]

#Creating the figure size for Bargraph
plt.figure(figsize=(20,10))
plt.scatter(x_axis, y_axis, marker = "o", color = "green")
plt.xlabel("Certificate")
plt.ylabel("Average Rating")
plt.grid()
plt.title("IMDB Rating scores by certificate")

#Saving as a JPG
plt.savefig('rating_scatter_graph.jpg', format='jpeg')