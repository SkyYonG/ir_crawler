### Web crawler that collects IR reports from "https://m.irgo.co.kr/IR%EC%9E%90%EB%A3%8C"

### 1. Overview

The crawler collects ir data from the previous day, processes it into the required form and stores it in a csv file. The data stored in csv is stored together in Mongodb for backup.

From the site above, the crawler enters the page with date "1일전" and collects data.

<img src="./main.png" width="500" height="350">

◈ Data collected
1) corporate name
2) company code
3) date uploaded
4) link to download ir-material

◈ Stored data
1) corporate name
2) date uploaded
3) link to download ir-material
4) link to view the company's financial statements (using company code)

### 2. How to use the jupyter_notebook file (ir_for_foreigners.ipynb)

Please use "ir_for_foreigners.ipynb". This is the most recent file I uploaded.

It's easy to use. Simply run the code in this file in order.

1) creat new project
2) writefile "items.py"
3) writefile "spiders.py"
4) writefile "mongodb.py" (please enter your own server address instead of ##.###.###.###)
5) writefile "pipelines.py"
6) writefile run.sh (a file that run the crawler, "run.sh" is stored in the folder where this jupiter_notebook file is located)
7) add "run.sh" file execution permissions to all users
