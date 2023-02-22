#Here is how the Spotify table was created.


CREATE TABLE BIT_DB.Spotifydata (
id integer PRIMARY KEY,
artist_name varchar NOT NULL,
track_name varchar NOT NULL,
track_id varchar NOT NULL,
popularity integer NOT NULL,
danceability decimal(4,3) NOT NULL,
energy decimal(4,3) NOT NULL,
song_key integer NOT NULL,
loudness decimal(5,3) NOT NULL,
song_mode integer NOT NULL,
speechiness decimal(5,4) NOT NULL,
acousticness decimal(6,5) NOT NULL,
instrumentalness text NOT NULL,
liveness decimal(5,4) NOT NULL,
valence decimal(4,3) NOT NULL,
tempo decimal(6,3) NOT NULL,
duration_ms integer NOT NULL,
time_signature integer NOT NULL )


#I then started to answer a few questions regarding the Spotify data.


#Question 1: 
What is the average danceability by artist and track?


SELECT AVG(danceability), artist_name, track_name
FROM BIT_DB.Spotifydata
GROUP BY artist_name


#Question 2:
Who are the top 10 artists based on popularity?


SELECT MAX(popularity), artist_name
FROM BIT_DB.Spotifydata
GROUP BY artist_name
ORDER BY popularity DESC
LIMIT 10


#Question 3:
What artist released the longest song?


SELECT MAX(duration_MS), artist_name, track_name
FROM BIT_DB.Spotifydata
ORDER BY duration_MS DESC
LIMIT 1


#Question 4:
What's the average danceability for the 10 most popular songs?


SELECT MAX(popularity), AVG(danceability), artist_name, track_name, danceability
FROM BIT_DB.Spotifydata
GROUP BY artist_name
ORDER BY popularity DESC
LIMIT 10
