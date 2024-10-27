**SUPPLY CHAIN NETWORK OPTIMISATION**

**Goal:** To optimise the supply chain network and visualize the results on a map.

**Given information**
1.	1 Port – Hamburg port
2.	3 DCs – Bremen, Berlin, Stuttgart. Each DC has a fixed cost ($10,000,000$) for setup and operations. It can handle an unlimited number of quantities.
3.	28 customers – Hanover, Rostock, Kiel, Trier, Karlsruhe etc. All customers are situated in German cities. Each city has a specific demand quantity (1000 units) which must be exactly met.
4.	Cost of transporting per quantity per kilometre is given.  c = 200$

**Methodology**
1.	Load an Excel file containing a list of port, DC cities and customer cities along with fixed costs associated with opening a particular DC and each customer's demand.
2.	Get the location (latitude, longitude) of each port city, DC city and customer city.
3.	Find the best road route and corresponding distance between each combination of port city and DC city. Also, find the best road route and corresponding distance between each combination of DC city and customer city.
4.	Run the optimisation model to get results.
5.	Visualising the optimized network of DCs and flows on a map.

**Libraries used**
Geopy, openrouteservices, gurobipy, pandas, folium

**Advantages/Strengths**
1.	Any number of DC city with fixed cost of operation can be loaded in the optimisation model.
2.	Any number of customer cities with fixed demand can be loaded in the optimisation model.
3.	The model will provide a city where DC should be setup and what customer cities will be catered by which DC city.
4.	The model will provide the total cost along with different cost drivers.
5.	The results are viewed on a map. It helps users to easily visualise the location of the port, DC city, and customer city along with the quantity flow.

![Image](https://github.com/user-attachments/assets/37a57ed9-6248-4dd9-8143-3beac9af445e)

**Limitations**
1.	The optimization model only supports 1 port.
2.	Each DC has a fixed cost.
3.	DC can handle unlimited quantities.
4.  The model used one cost of transportation for all routes. 

**Future scope**
1.	The optimization model can be further improved to support multiple ports in the optimisation model.
2.	Step cost can be introduced for DCs i.e., the cost of operating a DC will depend in which range the DC is handling the quantities.
3.  The model can have separate cost of transportation. Lower cost from port to DC and a slightly higher cost from DC to customers

