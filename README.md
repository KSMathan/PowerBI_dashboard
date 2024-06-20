
# Real-time water & weather data system - Dashboard

### Dashboard snapshot : 
Due to confidentiality issues, I'm not supposed to share the dashboard link.

![image](https://github.com/KSMathan/My_projects/assets/145895152/d875fd35-e671-44c0-9746-77237adde094)


## Problem Statement

This dashboard helps CII to monitor water consumption and weather data on a real-time basis. They want to understand the timely trend of weather parameters over the day. They have a rainwater collection tank, whose water presence needs to be known frequently. Moreover, they have four water feeding units namely water consumption unit, water reuse unit, water recharge unit and water recycle unit, whose feeding quantity need to be understood. This dashboard will be displayed on an LED screen kept at their common space in their institute, which helps the authorities to effectively monitor the water usage and weather.


### Steps followed 

- Step 1 : PostgreSQL database is connected to Power BI desktop and required database tables are loaded.
- Step 2 : Raw dataset is transformed into the desired dataset required to be projected onto the dashboard. In the power query editor, data transformation such as Add conditional columns, Filter rows, Change data type are done and proceeded to report view.
![image](https://github.com/KSMathan/My_projects/assets/145895152/4b25b681-0ad6-4234-9674-e1fb0a7bbbb4)
- Step 3 : Today’s weather data is represented as scorecards using card(new) visuals. Corresponding fields are dragged into the visuals and respective aggregations (rainfall-sum; Temperature-min,max; Humidity-min,max; wind speed-average; wind direction- a new measure is added to calculate mode of values in a day) are applied and in filter pane for this visual, the date field is filtered as filter type = ‘Relative date’ which is set to ‘in this day’. Suitable gif images are added and formatted under ‘Images’ option.
![image](https://github.com/KSMathan/My_projects/assets/145895152/62408ecd-02fc-4f62-879f-2e0efecc7aab)
- Step 4 : Hourly Weather trend is showcased over a line chart, which includes Rainfall, Temperature, Humidity and Wind speed. Same date filter as step-3 is implemented. 
- Step 5 : To represent the rainwater collection tank, since the client asked for an animated water tank visual, a visual called “Liquid fill gauge” is imported from an external source.
![image](https://github.com/KSMathan/My_projects/assets/145895152/b36d6144-39a1-48ad-8a66-4dec18cc366d)

    Note: This is an animated visual where the water level will raise to the level and remain waving.
- Step 6 : The water feeding units are represented as hourly data in the clustered column charts having the same date filter as the previous visual.
- Step 7 : Two text boxes are inserted at the top to include the title of the page and client’s logos. 
- Step 8 : The visuals which have labels named as months (e.g.June) are done by formatting suitable functions in titles and labels of visuals, which will be dynamic instead of having fixed text. 
![funct](https://github.com/KSMathan/My_projects/assets/145895152/d8e42667-f331-46de-a8b0-66129ecced48)
 - Step 9 : The report was then published to Power BI Service.
![image](https://github.com/KSMathan/My_projects/assets/145895152/1b40a242-040a-4d10-a2db-7ebf86daeff6)
 - Step 10 : In power BI service, it is data source connections signed in properly to fetch data directly from databases.
 - Step 11 : The report is embedded onto the google site using the “Published to web” option. In canvas settings, the height and width of the report is adjusted to fit the dashboard onto the client's LED screen.
 ![image](https://github.com/KSMathan/My_projects/assets/145895152/cf89b64e-91a0-4e7b-b561-da0b1a590ddb)
 - Step 12 : Refresh is scheduled for every 1 hour interval under the semantic model tab.
 ![image](https://github.com/KSMathan/My_projects/assets/145895152/8974a957-7595-44cf-a45d-61aca4fe11b6)
 - Step 13 : The automatic refresh of google site is achieved externally using a html script having the function to auto-refresh the site.
 ![image](https://github.com/KSMathan/My_projects/assets/145895152/67d431ca-96a5-4431-9d36-d80245068ef2)

