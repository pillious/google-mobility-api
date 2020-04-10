# Google Mobility Report Api
Get Google's [COVID-19 Community Mobility Reports](https://www.google.com/covid19/mobility/) data in Json form. <br>
* These reports provide data for changes in movement trends across the world. <br> (e.g.  Belgium has seen a 62% decrease in the amount of people going to parks.) 
<br><br>

[Find me on RapidAPI!](https://rapidapi.com/pillious/api/google-mobility-data)

## Usage: 
### Get data (json)<br>
https://google-mobility.now.sh/api/data

### Utility endpoints
All countries currently available - [/api/dates/names](https://google-mobility.now.sh/api/data/names) <br>
Available report dates - [/api/data/dates](https://google-mobility.now.sh/api/data/dates)
<br><br><br>
### Query parameters

https://google-mobility.now.sh/api/data?{parameters}

Parameter | Type | Description
------------ | ------------- | -------------
name | String | Search for a single country.
reportDate | Date | Get data for a single day<br>(format: YYYY-MM-DD)

<br><br>
Response example <br>
https://google-mobility.pillious.now.sh/api/data?date=2020-03-29&name=Aruba
```javascript
[
    {
        "data": [
            <!-- "change" represents percent change -->
            {"type":"Retail & recreation","change":"-88"},
            {"type":"Grocery & pharmacy","change":"-66"},
            {"type":"Parks","change":"-80"},
            {"type":"Transit stations","change":"-88"},
            {"type":"Workplaces","change":"-72"},   
            {"type":"Residential","change":"20"}
        ],
        <!-- regions provide more specific data -->
        "regions":[],
        "name":"ARUBA",
        "date":"2020-03-29T00:00:00.000Z"
    }
]
```

