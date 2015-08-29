
Using API to access third party data
========
This repository contains some details on the talk that I gave at `CUSP City Challenge Week 2015`.
We used the wifi hotspot data provided as one of the datasets at [`nycopendata.socrata.com`](https://nycopendata.socrata.com/) and `pygmaps.py` module that we will be using for plotting the output on google maps. `pygmaps` was initially created by Jiangyifei and is modified by me. 

## How to get API Endpoint
Socrata is a privately-held cloud software company that provides social data discovery services for opening government data. Its products are issued under a proprietary, closed, exclusive license but they do provide an API to access the open data. This API is known as SODA (Socrata Open Data Api) and for our this challenge we will be using `sodapy` which provides python bindings for the Socrata Open Data API

Socrata provides an online listing of [Socrata powered open data sites](https://opendata.socrata.com/dataset/Socrata-Customer-Spotlights/6wk3-4ija). All these sites have databases that can be accessed using their API (SDOA). 
> Once you’re on your local open data site, scroll down to the data catalog and use the search box and browse filters to find datasets that interest you. If your data site has custom API Foundry-managed APIs, you can use the “API” filter on the left-hand side to show only those custom APIs. But if your dataset doesn’t have the red API icon, don’t fret — every dataset is accessible via the SODA API. Click on Export and then API and you’ll find the API endpoint under API Access Endpoint. Copy that and save it for later.
> ![Accessing API Endpoint](http://dev.socrata.com/img/sidebar.gif)

In this workshop, we used the [NYC Open Wifi Hotspot data](https://nycopendata.socrata.com/City-Government/NYC-Wi-Fi-Hotspot-Locations/yjub-udmw?). However to access the data that this visualization is using, we need to use link that is called as API Endpoint. The endpoint of a SODA API is simply a unique URL that represents an object or collection of objects. A sample URL looks like this: `http://data.cityofnewyork.us/resource/yjub-udmw`
>Every Socrata dataset, and even every individual data record, has its own endpoint. The endpoint is what you’ll point your HTTP client at to interact with data resources.
>You can also find API endpoints in the “Developers” section of Socrata-powered data sites, or under “Export” then “API” on any Socrata dataset page, along with a link to the documentation for that specific dataset API.

## Installation
We have to install `sodapy` and `pygmaps`. 
### Install Sodapy:

- `pip install sodapy`

### Clone this repo:

- `git clone https://github.com/Mohitsharma44/talk_cusp_api.git`

## Use
Create your account at [socrata](https://nycopendata.socrata.com/signup) and login.

After logging in, scroll at the bottom and on the applications panel click on Manage -> Create a New Application. Enter the information about your new app (You can leave the URL fields empty.)

Fire up your ipython notebooks in the directory where you cloned this repo.

Check the [WifiHotspots](https://github.com/Mohitsharma44/talk_cusp_api/blob/master/wifi_hotspots.ipynb) example.
