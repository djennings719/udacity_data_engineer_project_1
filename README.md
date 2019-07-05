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

### Song 
#### song_id   - varchar
#### title     - varchar   
#### artist_id - varchar 
#### year      - int
#### duration  - numeric

### Artist
#### artist_id  varchar
#### name       varchar
#### location   varchar
#### latitude   numeric
#### longitude  numeric

### Time
#### start_time time
#### hour      int
#### day       int
#### week      int
#### month     int
#### year      int
#### weekday   int

### User
#### user_id    int
#### first_name varchar
#### last_name  varchar
#### gender     varchar
#### level      varchar
#### visits     int

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
