# GIS-For-Conservation
Using GIS to determine which roads should be shut down in an effort to conserve the Storm Wing Falcon population in Arizona.


I. Statement of Problem
&nbsp;&nbsp;&nbsp;&nbsp;A. Discipline: Conservation: Storm Wing Falcon Populations in Arizona. I’m going to choose this topic because I’m passionate about animals and conservation. The human population is only going to grow as time goes on, so I believe that it is very important to have environmental scientists using software like GIS to help find ways to prevent endangerment and extinction of the earth’s several species.   
&nbsp;&nbsp;&nbsp;&nbsp;B. Question: The question I am looking to solve is “Which roads should be shut down during the storm wing falcon breeding season?” The state wants a series of maps to identify roads within a half mile of the storm wing falcon breeding areas on federal land to shut those roads down during breeding season. I will use GIS spatial techniques to identify where the breeding areas are. I will then use spatial techniques to identify and exclude interstates, major highways, or state routes from the map. The state can only shut down on roads that are not privately owned, so I will only make sure to include only state-owned roads. Lastly, I will use GIS spatial techniques to exclude roads that are on Native American reservations. It will also be helpful to consider the location of turquoise bellied snail territories because it is the only food that the storm wing falcons will eat during breeding season. This type of snail is only found on soil that contains dacite as part of the geological composition, so I can use GIS data to determine what types of soil are present in the area. I plan of using the internet to search for reputable data tables on these subjects.   
&nbsp;&nbsp;&nbsp;&nbsp;For special deliverables, I will need to provide a map of storm wing falcon breeding areas, a map of turquoise bellied snail territory, provide multiple maps of road closures at appropriate scale, and provide a map of total road closures.   

II. Data
&nbsp;&nbsp;&nbsp;&nbsp;A. Spatial Data: There is a lot of information available, so I wanted to select the information that was most relevant to the problem and that answered my question “Which roads should be shut down during the storm wing falcon breeding season?” to make sure the map was not too crowded. Under the folder AZ Administration, I found the AZ State Outline and added that to the map. Next, under the Transportation folder, I added the interstates and highways because the state will not close those. I also thought it was important to add the main roads since those are the only ones that can be closed. Then, under the AZ Administration folder, I added information about the Reservations since the state cannot close roads on the reservations. I added state parks because I figured that could be a good place for the storm wing falcons since there’s a lot of natural land there. Finally, I added information about the geology under the Environment folder since the storm wing falcons will only eat the turquoise bellied snail during breeding season, and that snail resides on soil that contains dacite.   
&nbsp;&nbsp;&nbsp;&nbsp;The spatial data type that I will be using will be called a vector model because it relies on x-y coordinate locations to store information and then present it on the map. The two different vector objects that will be used will be lines for the different types of roads and polygons for the reservations, state parks, and geology. The raster model, as contrast, contains cells or pixels that contain a numeric code indicating a single attribute.   
&nbsp;&nbsp;&nbsp;&nbsp;B. Organization: I decided to put the interstates and the highways in red to show myself that I could not use them. I made the main roads and state parks a green color to symbolize that I want to use them. The reservations I made red as well. The turquoise bellied snail is only found on soil that contains dacite, so I opened the geology table and did the query “ROCKTYPE2 = dacite.” Then I did “Select by Location” to search for areas within one mile of dacite, which is the location for ideal breeding nests. This showed all the areas in bright blue, and it made it really easy to see where my breeding locations could be.   
&nbsp;&nbsp;&nbsp;&nbsp;C. Quality: My data is reliable and is from a trusted source. I compared the geographical data that I received from this course to data that I found on a GIS map on roads and reservations from az.gov and it matched the data that I found from the class.   
&nbsp;&nbsp;&nbsp;&nbsp;The quality of the data can be affected, for example, if you add data to the map that does not have the same coordinate system. This could be a major issue with this project, especially, since the distance of the breeding nests from the turquoise bellied snails (1 mile) is so short that not having the right coordinate system could easily throw off which roads to close.   

III. Methodologies 
&nbsp;&nbsp;&nbsp;&nbsp;A. Outline: I was able to find all my data under the final project database, so I didn’t have to convert much data. The only conversion I ran into was when I added the reservations. The reservations weren’t in the same coordinate system as my other data, so I had to make sure that it was the same one. When I tried to add the reservation data, a box came up warning me that the geographic system of the data was different than the data frame I was adding it to. I clicked the “Transformations…” box and converted the current system, GCS_North_American_1983, into GCS_NAD_1983_2011.   
&nbsp;&nbsp;&nbsp;&nbsp;B. Data Set(s): The data sets I added were the ones that I felt were most relevant to my problem since I didn’t want the map to become too crowded. I added the interstates, highways, main roads, geology, state parks, and reservations. All of these were found under the final project database. I felt that it was all the information that I needed to answer my question, “Which roads should be shut down during breeding season?” To add the data, I simply clicked the “Add Data” button in ArcMap and found them under the final project data folder. When I selected which file I wanted, I clicked “Add” and it added the layer to the map.   
&nbsp;&nbsp;&nbsp;&nbsp;C. Geoprocessing Tools: First, I selected dacite by using the query “ROCKTYPE2 = dacite” since dacite is the location for ideal breeding nests. I decided to use the buffer tool so that I could see the areas that are within one mile of dacite, using geology as the input feature. Next, I decided to use the intersect tool to find the common area between the main roads and the dacite (geology buffer). Then I selected then reservation tab one more time to make sure that none of these roads were on the reservations. Doing this, it is very easy to see which main roads should be closed because they lead to the breeding areas.   
