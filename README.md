# Data Engineer Projet 1

## How to run the project
### Ensure that you have no current connections to the database open.
#### If you have just been in Jupyter notebook open the Kernel menu and click on Restart Kernel

### From the command line > python create_scripts.py
#### This will delete and re-create the database schema

### From the command line > python etl.py
#### This will execute the etl process.
#### First it will process the song data followed by the log data

## Background

#### Sparkify requires the ability to analyze data regarding which songs are being played.  

## Reasoning for database schema



### Song 
#### Dimension table
#### song_id   - varchar - this is due to data values
#### title     - varchar   
#### artist_id - varchar 
#### year      - int
#### duration  - numeric

### Artist
#### Dimension  table
#### artist_id  varchar
#### name       varchar
#### location   varchar
#### latitude   numeric
#### longitude  numeric

### Time
#### Dimension table
#### start_time time
#### hour      int
#### day       int
#### week      int
#### month     int
#### year      int
#### weekday   int

### User
#### Dimension table
#### user_id    int
#### first_name varchar
#### last_name  varchar
#### gender     varchar
#### level      varchar
#### visits     int

songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
### Songplay
#### Fact table
#### songplay_id serial - for primary key incrementing
#### start_time  time
#### user_id     int
#### level       varchar
#### song_id     varchar
#### artist_id   varchar
#### session_id  int
#### location    varchar
#### user_agent  varchar