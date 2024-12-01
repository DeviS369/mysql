IMDB Database Design
Overview
This project designs an IMDB-like database using My. It manages movies, genres, media, users, reviews, and artists, fulfilling complex relationships and ensuring proper normalization with primary and foreign keys.Features
Supports Movies with Multiple Media:A movie can have images and videos.
Multiple Genres:A movie can belong to multiple genres via a many-to-many relationship.
User Reviews:Reviews are tied to both users and movies.
Artist Skills:Artists can have multiple skills and perform multiple roles in movies.
Data Relationships:Proper normalization ensures data consistency.
Tables and Relationships
Movies: Stores movie details.
Media: Stores media linked to movies.
Genres: Lists all genres.
Users: Lists users who can leave reviews.
Reviews: Connects users with their reviews for movies.
Artists: Lists all artists involved in movies.
Artist_Skills: Links artists to their skills.
Movie_Artists: Links artists to their roles in specific movies.
How to Use
Create Database:CREATE DATABASE IMDB;
Run Table Scripts: Execute the provided  scripts to create tables and relationships.Insert Data: Use the sample data scripts for testing or insert custom data.Execute Queries: Fetch data as needed using the query examples.Sample Queries
Get all media for a movie:SELECT m.title, md.media_type, md.url
FROM Movies m
JOIN Media md ON m.id = md.movie_id
WHERE m.title = 'Inception';
Find roles of an artist in a movie:SELECT ma.role
FROM Movie_Artists ma
WHERE ma.movie_id = 1 AND ma.artist_id = 1;
Author
Designed to showcase advanced My relational database management for an IMDB-like application.
