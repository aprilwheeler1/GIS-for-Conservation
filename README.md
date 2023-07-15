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

<img width="403" alt="image" src="https://github.com/aprilwheeler1/Remote-Sensing-the-City-of-Los-Angeles/assets/102776972/a804dec5-e017-46fd-b5de-54b51a7d893d">   
<div style="page-break-after: always;"></div>
<div style="page-break-after: always;"></div>

<img width="395" alt="image" src="https://github.com/aprilwheeler1/Remote-Sensing-the-City-of-Los-Angeles/assets/102776972/086ae61b-effb-4f5c-9c4d-a972306f431f">   

&nbsp;&nbsp;&nbsp;&nbsp;D. Symbols: I decided to stick with lines for all the roads, since roads are lines anyway. I color coded the interstates and highways as red since I couldn’t shut those down, and I used green for the main roads since I could shut those down. The reservations and the parks I kept true to shape and made the reservations red and the parks green. The geology buffer and main roads intersection I kept green to show that I could use those roads.

<img width="404" alt="image" src="https://github.com/aprilwheeler1/Remote-Sensing-the-City-of-Los-Angeles/assets/102776972/c6184593-3571-4a98-8466-dff75bf0afe9">

&nbsp;&nbsp;&nbsp;&nbsp;E. Map:

<img width="395" alt="image" src="https://github.com/aprilwheeler1/Remote-Sensing-the-City-of-Los-Angeles/assets/102776972/13b30cab-d4fa-4afa-ab20-ec0d01c9abde">

The green lines are the main roads that intersect between the 1-mile geology buffer (dacite) and the main roads layer.

&nbsp;&nbsp;&nbsp;&nbsp;F. Best Practices: For best practices, I tried to incorporate all the basic elements of map design such as visual contrast, legibility, figure-ground, hierarchical organization, and balance. I wanted there to be a visual contrast between the green “yes” areas and the red “no” areas, and in my opinion, the visual contrast and the colors used was appropriate for the purpose of my map. I think my map was legible because of the good visual contrast and because it was not too crowded. The use of lines for roads and polygons for bigger areas of land made sense to me. I thought the figure-ground did a good job of outlining the state and the different areas and boundaries. I think my map had great hierarchical organization which is apparent in its main priority and purpose: which roads should be shut down during breeding season. There were so many other details about Arizona I could’ve added such as hospitals, businesses, shopping malls, etc. but I thought doing so would interfere with my hierarchical organization. I thought my map was balanced and all the parts of the map took up the appropriate amount of space.   
&nbsp;&nbsp;&nbsp;&nbsp;I struggled at first with using the intersect tool. At first it would not create a new later. After doing some research I found out that I needed to go to Geoprocessing > Geoprocessing Options > and uncheck “Background Processing.” After that it worked. I tried to make my map organized, not too crowded, and color coded so that the viewer could see “green = yes, shut down” and “red = no, don’t shut down.”

IV. Conclusions
&nbsp;&nbsp;&nbsp;&nbsp;Observations: When I observe my map, I can see that only a small amount of roads are available for closure. A large portion of the state is off limits because of reservations. There is basically either a highway or an interstate at all areas of the state, so that makes it another challenge. The mineral dacite is also abundant in areas of the state, such as the northwest and the southeast, where many roads cannot be shut down because of the little access to the appropriate roads for shut down.   
&nbsp;&nbsp;&nbsp;&nbsp;Recommendations: Observing my map and seeing how little roads are available for closure under these guidelines, I can see why the storm wing falcon population of Arizona is endangered. It is a challenge to meet the quality of life and the dietary restrictions of these birds and to coexist with humans at the same time. Perhaps more of an effort can be made to prop up the bird population in other ways. If more dacite/turquoise bellied snails are deposited throughout places in the state they wouldn’t normally be, such as the state parks, maybe that would provide much more land for the storm wing falcons to prosper. I think that the state of Arizona should do everything it can to try to save this species and its important role in the ecosystem in order to prevent more eventual effects from climate change. Utilizing the state parks for natural land for these birds would be a great first step.


References

Buckley, Aileen. Design Principles for Cartography. 28 October 2011. Retrieved from https://www.esri.com/arcgis-blog/products/product/mapping/design-principles-for-cartography/

Intersect Tool Issues. 28 July 2017. Retrieved from 	https://community.esri.com/t5/geoprocessing-questions/intersect-tool-issues/td-p/283511

Maps & GIS. Arizona State Land Department. Retrieved from https://land.az.gov/maps-gis-0

