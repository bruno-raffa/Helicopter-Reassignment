 X - Coord Y-Coord # Assigned Projected Demand Location #1 36 20 6 7 Location #2 23 30 2 3 Location #3 23 56 3 2 Location #4 10 15 3 4 Location #5 5 5 4 2 



Air Ambulance Reassignment Problem
This project solves an Air Ambulance Reassignment Problem using a hybrid quantum-classical approach. The problem is to reassign air ambulances in order to meet changing demand projections. The approach used here involves using a Constrained Quadratic Model (CQM) that is formulated as a Quadratic Unconstrained Binary Optimization (QUBO) problem. The solution is computed using the LeapHybridCQMSampler.

The problem is defined here is defined here: https://miro.neos-server.org/app/airambulance.

an air ambulance (helicopter) service provider has a set of locations with a number of helicopters assigned to each site. Within each site's defined service area, requests are satisfied by the helicopters assigned to that site. At the end of each time period, the service provider updates the projected demand for each site and determines whether any of the helicopters need to be reassigned. There is a transportation cost associated with reassigning a helicopter to a different site. Therefore, the service provider wants to determine a minimum cost assignment of helicopters to sites to satisfy the next period's projected demand at each site. 

As an example, consider an air ambulance service provider with 5 locations in the Midwest. The company evaluates the need to relocate helicopters based on the monthly projected demand for each location. The cost of reassigning a helicopter from site ii to site jj is $100 per kilometer of distance from site (i) to site (j). For each of the company's locations, the table below lists the (x) and (y) coordinates of the site, the number of helicopters currently assigned, and the projected demand for the next period. To make the toy example more realistic some randomly midwest cities were assigned to the Locations. The coordinates do not pertain to the cities, the names were assigned just for didactic purposes to reflect a real case where the name of the locations are known

Installation
This project requires the following Python packages to be installed:

dwave-system
dimod
dotenv
networkx
pandas
numpy
matplotlib
To install these dependencies, run:

Copy code
pip install -r requirements.txt
Usage
Load the environmental variables by running load_dotenv(find_dotenv()).
Import the data by running with open('locations.csv', 'r') as f.
Reshape the initial data format in a more useful structure by running summarize_data(locations).
Build the Constrained Quadratic Model by running build_cqm(locations).
Sample the CQM by running sample(cqm).
Parse the sample data by running parse_data(data).
Restructure the locations dictionary by running restructure_locations_dict(locations_dict).
Draw the graph with arrows by running draw_graph_with_arrows(coords_dict, routes_data).
Code
The code is structured as follows:

Import necessary libraries
Load environmental variables
Import the data
Reshape the initial data format in a more useful structure
Build the Constrained Quadratic Model
Sample the CQM
Parse the sample data
Restructure the locations dictionary
Draw the graph with arrows.



