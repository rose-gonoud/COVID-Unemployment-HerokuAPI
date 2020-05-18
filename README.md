# Unemployment Data in the Age of COVID-19, Project 2

### Unemployment Data during COVID-19

This is the repository attached to the US Unemployment Data API that feeds into the main project, described below and featured here: https://github.com/rose-gonoud/COVID-19-Predictive-Modelling

We are officially live at https://unemployment-during-covid19.herokuapp.com/

### Overall Project Scope and Objective

This work displays US unemployment data from 2019 through the present day in a responsive browser dashboard. Its primary feature is a map containg US unemployment data claim numbers, broken down by state and visualized using a color-coded gradient system. Each state's total number of unemployment claims for a user-selected period of time will display as an aggregate - that is, the entirety of any given state will be represented as a single color.

An additional map layer represents the number of COVID-19 related deaths each state has experienced through the present day. This code pulls from a publically hosted API (https://rapidapi.com/axisbits-axisbits-default/api/covid-19-statistics) in real time, so that our dashboard's data is always as updated as its source. Code for this particular layer was adapted from our collaborator Jesse Caldwell's personal repository: https://github.com/CollectionOfAtoms/covid_visualization.

Data may be filtered by custom date ranges and a custom multi-select state menu (rendering data for any single state or possible combination of multiple states). This dashboard also contains line graph visualizations for both total claim numbers and unemployment rates, responsive to the same combinations of filters above. All dashboard interfaces update in unison in response to user input.

Linked on the navigation bar, there is an additional data table allowing the user to browse our raw numerical data.

### Our Tools

https://oui.doleta.gov/unemploy/claims.asp

The above link provided us with the raw unemployment data - it was downloaded as a CSV, and will be uploaded row by row into a MongoDB collection. Our flask app will read information from the database based on user input from our webpage/visual dashboard, and initialize real-time updates our dashboard with the result of the mongo query.
