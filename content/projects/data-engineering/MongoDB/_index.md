---
title: "MongoDB"
draft: false
summary: "Database for a Movie Recommendation System"
---


A full-stack movie recommendation system built by a team of 4, combining MongoDB for data management, Flask API for serving predictions, and a frontend for user interaction. MongoDB played a critical role as the database layer—storing cleaned datasets, enabling efficient queries, and acting as the bridge between raw movie/user data and the ML-powered recommendations.

## Data Flow
{{< gallery >}} 
<img src="static/images/movie-details-list.png" alt="Movie Details"> 
<img src="static/images/movie-list.png" alt="Movie List">
{{< /gallery >}}
- Raw data was collected, cleaned and transformed in Python.
- Stored structured collections in MongoDB.
- Mongo served as the central data hub, queried by Flask to power recommendations.

## MongoDB Schema
Standard JSON Format
{{<video src="static/videos/standard-json.mp4" autoplay="true" width="400" loop="true" >}}
MongoDB Format
{{<video src="static/videos/mongo-json.mp4" autoplay="true" width="400" loop="true" >}}
- Collections: movie details (titles, genres, overview, poster paths).
- Collections: user preferences (IDs, ratings, interaction history).
- A flexible MongoDB schema allowed for easy addition of new features and data sources.
- No rigid schema, allowing for fast iteration during preprocessing and model tuning.

## Flask API to MongoDB
![Mongo Connect](static/images/mongo-connect.png)
- Flask API connects to MongoDB (pymongo/MongoClient).
- Queries user history and movie features directly form Mongo collecitons.
- Ensures real-time data access for personalized recommendations.

## Example Query in MongoDB (Aggregation Pipeline)
![Mongo Aggregation](static/images/aggregations.png)
- Used aggregations in Mongo to filter through collections.

## Endpoint
- User enters ID, frontend sends request to Flask API.
- Flask retrieves data from MongoDB colections, runs ML models, returns recommendations.
- Mongo connects the raw data to the personalized predictions.


---
You can find the code for this project in my
[Github Repo](https://github.com/Chan-McLaren/Movie_Recommendation_Model)

---
[Back to Data Engineering]({{< relref "../_index.md" >}})