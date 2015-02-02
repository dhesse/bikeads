Targeted bicycle advertising
============================

An on-line version of this notebook can be found [here](http://nbviewer.ipython.org/github/dhesse/bikeads/blob/master/bike_ad_project.ipynb).

Summary
-------

The goal is to increase the impact of advertising that is placed on
shared bicycles. We suggest employing collected bike-sharing trip data
to develop a system that would make a prediction where a given
customer taking a bicycle will most likely travel to and select a bike
with relevant advertising for the population in that zone. Exploratory
analysis of bike trip data collected in San Francisco shows that the
goal is well within reach.

Project description
-------------------

Many cities around the world run bike-sharing programs, which yield
many benefits like reduced traffic and increased citizen's health. In
some cities, these programs are run by advertising companies who use
the bikes to display ads. In some cases however, all bikes carry the
same advertising, which may not be relevant to all demographic
groups. Given a sample of trip data, one can even with minimal
information on the kind of customer wanting to take a bike make some
prediction where he or she will likely travel to. In the case of the
San Francisco bike sharing program the collected information contains
among others the kind of subscription (yearly subscription or 1-3 days
pass), and in the case of a yearly subscriber the zip code, which as
we will see is ample information to make an informed prediction. With
the knowledge where the trip will end, we can calculate the most
probable route and choose a bike with an ad aimed at the demographic
likely to be encountered. This seems like an attractive aim since the
visibility of ads on bicycles is highest when on the street as opposed
to on a bike rack.

Exploratory data analysis
-------------------------

For the first analysis, trip data acquired by the San Francisco bike
sharing program [1] is used. To obtain a good sample size, all trips
originating from the station that is the most frequent starting point
(San Francisco Caltrain (Townsend at 4th)) is used and split into
trips of customers (those with a one- or three-day pass) and
subscribers (those with an annual pass). To illustrate the emerging
pattern, we plot the number of trips to a various destinations,
labelled by a numerical id rather than the full name [2,3]. It comes
as no surprise that customers, who probably are tourists or other
short-term visitors prefer to go to different locations than
subscribers. To give an example, stations 50, 60, and 70 are the most
popular among customers, while 60 and 70 are among the least popular
among subscribers. There are similar patterns where popular subscriber
destinations are not popular among customers, which is again
unsurprising. Few tourists will visit residential areas. Since in the
case of subscribers we also have their zip codes available, we can
push our analysis further and break the destination data down by zip
code. For the plot [4] only the five most common zip codes were
considered to keep the plot clean. Also here clear patterns
emerge. For instance, station 54 is visited predominantly by customers
with zip code 94105 (green in the figure), hinting at the fact that
the station lies within that zip code.

Future plans
------------

The data broken down by customer data should now be augmented by
demographic information to find the most suitable kind of advertising
for a given trip. A suitable learning algorithm to predict the most
probable destination for a given customer type and starting station
might be a decision tree. The downside of this method would be that
the tree will have to be re-generated once a new station is added or
more customer information becomes available.

Conclusion
----------

We have seen that predicting destinations given a customer type and
starting station is feasible and targeted bike advertising a promising
possibility.


References
----------

[1]: http://www.bayareabikeshare.com/datachallenge
[2]: https://drive.google.com/file/d/0B_jDmEo73f0mcGNfX2ZTT1BaYm8/view?usp=sharing
[3]: https://drive.google.com/file/d/0B_jDmEo73f0mQW1pSjctRG5fdHM/view?usp=sharing
[4]: https://drive.google.com/file/d/0B_jDmEo73f0mSmVUNFRDUDNRY2c/view?usp=sharing
