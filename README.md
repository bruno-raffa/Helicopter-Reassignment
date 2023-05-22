 ## Air Ambulance Reassignment Problem
This project solves an Air Ambulance Reassignment Problem using a hybrid quantum-classical approach. The problem is to reassign air ambulances in order to meet changing demand projections. The approach used here involves the use of a Constrained Quadratic Model (CQM). The solution is computed using the LeapHybridCQMSampler from dvawe (https://cloud.dwavesys.com/)

The problem is defined here: https://miro.neos-server.org/app/airambulance.

An air ambulance (helicopter) service provider has a set of locations with a number of helicopters assigned to each site. Within each site's defined service area, requests are satisfied by the helicopters assigned to that site. At the end of each time period, the service provider updates the projected demand for each site and determines whether any of the helicopters need to be reassigned. There is a transportation cost associated with reassigning a helicopter to a different site. Therefore, the service provider wants to determine a minimum cost assignment of helicopters to sites to satisfy the next period's projected demand at each site. 

As an example, consider an air ambulance service provider with 5 locations in the Midwest. The company evaluates the need to relocate helicopters based on the monthly projected demand for each location. The cost of reassigning a helicopter from site ii to site jj is $100 per kilometer of distance from site (i) to site (j). For each of the company's locations, the table below lists the (x) and (y) coordinates of the site, the number of helicopters currently assigned, and the projected demand for the next period. To make the toy example more realistic some randomly midwest cities were assigned to the Locations. The coordinates do not pertain to the cities, the names were assigned just for didactic purposes to reflect a real case where the name of the locations are known.



