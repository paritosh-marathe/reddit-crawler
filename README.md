# reddit-crawler

##  Introduction 
This repo is for holding the project Analyzing Topics, Framing, and Hate Speech in Online Political Engagement. 
The data is retrieved from reddit and 4chan boards. It uses Grafana as a dashboard for displaying the metrics. 
##  Data Retrieval
The data is retrieved from reddit and 4chan boards using the respective APIs .

## Screenshots 
![1](images\1.png)
![2](images\2.png)
![3](images\3.png)

## How to run 
---
navigate to project 
>conda activate trial (conda environment containing packages)
> python reddit_crawler.py
>python chan_crawler.py
>python _init_.py

# Troubleshoot 
___
Noted failure for booting faktory after ssh reload 
start stop redis for faktory 
> start-stop-daemon --stop --quiet --exec /usr/bin/redis-server <br>
> start-stop-daemon --start --quiet --exec /usr/bin/redis-server

run faktory in development mode :
> faktory -e development 

may require stopping faktory by killing process :
get pid by 
> lsof -i -n
mass murder stuff :
kill -9 $(lsof -t -i tcp:7419)