# Unemployment Data in the Age of COVID-19, Project 2

### Overall Project Scope and Objective

We intend to display nationwide unemployment data from 2019 through the present day, broken down by state. This data will be overlaid on a map, and visualized using a color-coded gradient system. Each state's total number of unemployment claims for a user-selected period of time (likely just by month?) will displayed as an aggregate - that is, the entirety of any given state will be represented as a single color.

We intend to display this map as part of a larger interactive dashboard. We imagine this dashboard will also have a data table the user can scroll through to view raw numerical data, and some sort of visualization (a scatter or bar chart).

We also plan to add a map layer representing the number of COVID-19 deaths per state up through the present day. So the density of unemployment claims would be prepresented by the color of the state on our map, and on top of that would be some indicaton of the number of COVID-19 deaths within that state to date.

We are playing with the idea of incorporating historical data that would be topically relevant (the 2008 recession, the 1918/19 flu epidemic's unemployment numbers, if they exist, etc.) but that is obviously a time-dependant addition.

### Our Tools

https://oui.doleta.gov/unemploy/claims.asp

The above link provided us with the raw unemployment data - it was downloaded as a CSV, and will be uploaded row by row into a MongoDB collection. Our flask app will read information from the database based on user input from our webpage/visual dashboard, and initialize real-time updates our dashboard with the result of the mongo query.

### Heroku Deployment

We are officially live at https://unemployment-during-covid19.herokuapp.com/
