README for Project 5 (group project)

# Notes
- Official column headers are here:
https://www.gdeltproject.org/data/lookups/CSV.header.dailyupdates.txt
- These are good for April 2013 - present so should be good for us

- Column headers in .xlsx format:
https://www.gdeltproject.org/data/lookups/CSV.header.fieldids.xlsx

#### The "tone" column is super interesting:
    "AvgTone. (numeric) This is the average “tone” of all documents containing one or more mentions of this event. The score ranges from -100 (extremely negative) to +100 (extremely positive). Common values range between -10 and +10, with 0 indicating neutral. This can be used as a method of filtering the “context” of events as a subtle measure of the importance of an event and as a proxy for the “impact” of that event. For example, a riot event with a slightly negative average tone is likely to have been a minor occurrence, whereas if it had an extremely negative average tone, it suggests a far more serious occurrence. A riot with a positive score likely suggests a very minor occurrence described in the context of a more positive narrative (such as a report of an attack occurring in a discussion of improving conditions on the ground in a country and how the number of attacks per day has been greatly reduced)."





# DOWNLOADS:
- MAY 5 raw CSV file here:
https://drive.google.com/open?id=1kP5tttaB41Qh1kZKLvkhL4TECdh9Alsl

- GDELT has about ten datasets. The one we looked at earlier today(Friday May 8) is the "GDELT 2.0 Event Database":
http://data.gdeltproject.org/events/index.html

- Overview of our dataset here
https://blog.gdeltproject.org/gdelt-2-0-our-global-world-in-realtime/

- Here's the full list of other datasets we could use:
https://blog.gdeltproject.org/the-datasets-of-gdelt-as-of-february-2016/

- We don't have to use AWS, they have other tools: https://www.gdeltproject.org/#downloading





# TO-DO list
- We need to download and concatenate the files
- We need to figure out whether we are downloading to our personal machines or doing it straight from AWS storage "S3 bucket"
- Need to figure out Geopandas or some other mapping system
- Last cohort's project had a good example for Colorado, but of course we are more interested in world domination:
https://github.com/magnusbig/fema_7_lifelines/blob/master/code/flood_zones.ipynb

- A good place to start might be to download one file from Jan, one from Feb...etc and then map them quickly so we know what we are dealing with.







# AWS:
- There are a LOT of AWS tools. Here are some:
https://us-east-2.console.aws.amazon.com/dataexchange/home?region=us-east-2#/

- The data is stored in "S3" which seems to be the most widely-used AWS storage product.

#### Some options for the computing part. All of these are going to require learning:
    - EC2 which is the most generic, this is what we demo'd in class
    - Athena which SQL queries stuff directly
    - Lambda which runs your code against the S3 data directly
    - Sagemaker which has ML tools for running it directly



- I saved EC2 directions below:




















# AWS TERMINAL COMMANDS:

#### SETUP
#### Terminal connecting to Server steps:
- Use security key:
sudo chmod 700 /path/to/key.pem

- Connect to server:
ssh -i /path/to/key./pm ubutnu@<<<public DNS from AWS>>>

- Install Anaconda:
wget http://repo.continuum.io/archive/Anaconda3-4.1.1-Linux-x86_64.sh

- Execute Installer 
bash <<<use tab to find file below>>>
    
- COPY SPACE AT END:
bash Anaconda3-4.1.1-Linux-x86_64.sh 

- Yes to all
Make sure to enter yes to install location to path in Home ubuntu

- Locate conda
source ~/.bashrc

- Optional??? Open bash rc
nano ~/bash.rc
    
#### NOW LETS GO

- LOCAL MACHINE:
THIS IS THE COMPLEX ONE - NOTE SPACES:
scp -i /path/to/key.pem /path/to/model.py ubuntu@<<<public DNS from AWS>>>:~

- CLOUD MACHINE:
Run File
python 3 model.py

- Edit File
nano model.py

- Rerun as needed


#### MOVE FILES FROM REMOTE TO LOCAL
scp -i /path/to/key.pem ubuntu@<<<DNS from AWS>>>:~/output.csv .

#### REMEMBER TO TERMINATE INSTANCE!!!
