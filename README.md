# XML Feed Parser & Post To Twitter

Built in Python, this program parses a given XML file/feed. 
We extract specific fields from the XML feed(such as title and url) and post that data to Twitter.


#Dependencies Required(naturally, some commands below only for apt management systems)

- apt-get install python3 python3-pip
- pip3 install requests
- pip3 install tweepy


#Editing Configuration

- All configuration is located within parse_xml.py

- Twitter API Credentials: This area is commented in the code file, here is a link on how to grab your API details. https://python-twitter.readthedocs.io/en/latest/getting_started.html

- 2022 Twitter API Update: Read the 2022 solution here which requires OAuth1 https://stackoverflow.com/questions/8389796/why-this-error-read-only-application-cannot-post

- Change the XML Feed to parse: You will see a url in the code file under this line '#Set the XML File/Feed to pull'. Just replace the url.

- Last note: Make sure the db.txt file exists even if its empty.


#How to run the program?

- From the terminal: python3 parse_xml.py
- From a cronjob: I personally create a trigger.sh file, within that file calls the python3 command to execute the file. Then I set the cronjob to trigger that trigger.sh file.
