**Overview:** This assignment is aimed at using our workflow (Collect, Clean, Analyze) to prepare data for analysis.

**Scenario:** A musicology researcher is interested in the locations of dance clubs in Los Angeles and wants to create a map of these; she is particularly interested in genres, so if you can get location and genre, that would be very nice.   You've discovered that Yelp is a pretty up-to-date source of information.  

**The Assignment:**  You want to scrape information on the names, addresses, and genres of LA Dance Clubs using Import.io.  Then you want to geocode the address (providing a couple of new columns -- lat & long) of each club based on the street address in OpenRefine.  The goal is to have a spreadsheet with name, address (lat & lon), genres in a spreadsheet that we can start using with Tableau.  

1. Collect:  Import.io.  You can do this assignment in the web-based Import.io. (The process will, however, be faster in the Import.io app.)   Although the web-based version appears to just give you the first 10 results,  you will find some functionality that allows you to add new URLs.  Notice that the results, in Yelp, spread over several pages.  You just keep adding slightly adjusted URLs into the program, scraping each successive page.  (I will post some screenshots in Slack.)   

a. https://www.yelp.com/search?find_desc=dance+clubs+&find_loc=Los+Angeles,+CA  
Put the above URL into Import.io
https://osf.io/2e6vr/

E.g.

https://www.yelp.com/search?find_desc=dance+clubs+&find_loc=Los+Angeles,+CA&start=10

https://www.yelp.com/search?find_desc=dance+clubs+&find_loc=Los+Angeles,+CA&start=20

30, 40, 50, etc.  

When you've added a whole batch of URLs, you save them, and then run the entire query.  After extracting data from each one, you'll be able to save the csv file.  The video above shows the process.  

In the next installment, geocoding in OpenRefine.

2. Clean: OpenRefine.  In this section, you'll open the csv file in OpenRefine -- and we'll merge two columns to create a FullAddress column, then, we'll geocode on the street address.  

a. Notice that we've got street addresses from Anaheim, Culver City, etc.  We've got street addresses that, in order to geocode, we'll need to combine Secondary 1 with Secondary 2.  To do this we'll use a regular expression (YAY!) to create a new column by combining (concatenating) those two columns.  

b. In drop-down menu for Secondary 2, choose Edit column >Add a column based on this column.  Name it fulladdress.  Then, in the expressions, enter  cells['Secondary 1'].value + ' ,' + cells['Secondary 2'].value  As you type the regular expression, you should see the results displayed in the box.  

Hit OK, and you should get a nice new column that combines the two others.

c.  Now, we want to create another new column for the latitude and longitude results.  From the fulladdress column, Edit column >Add column by fetching URLs.  We'll add this formula to call google's geocoding webservice:  "http://maps.google.com/maps/api/geocode/json?sensor=false&address=" + escape(value, "url")

d. wait.  this will take some time and you'll get a column filled with JSON code.  You will now parse this, extracting just one pair of lat/long coordinates.  You guessed it!  Edit column>Add column based on this column.  Then copy and paste in this formula:
with(value.parseJson().results[0].geometry.location, pair, pair.lat +", " + pair.lng

e. You should now have a nice column with a pair of coordinates.  Save your spreadsheet, and you're ready for some Tableau!  

If you've made it this far, you deserve some applause.  You've done a lot in both Import.io and OpenRefine.

If you're eager for more, try the same process with some other tools. (We're on the lookout for a replacement for Import.io) Chrome has a web-scraping extension that should accomplish the same sort of paginated scraping.  Let us know what works for you!  
