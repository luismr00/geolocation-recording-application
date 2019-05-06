# Geolocation Application

## Summary

An instructor has provided a list of cities and their geocoordinates (latitude and longitude) in JSON format. The instructor would like a web application which fetches the data and displays it to a user. The application should calculate the distance between Oregon State University and the city listed in the JSON. The instructor has provided a function for you to use for this purpose. Lastly, the rendered data should be sortable by ascending and descending calculated distance.

### Instructions

1. The web application should fetch the JSON at runtime from here:
https://s3-us-west-2.amazonaws.com/cdt-web-storage/cities.json

2. Calculate the distance between each city and OSU using this function:
[https://github.com/osuecampus/geolocation-recording-application/blob/master/distance.js](https://github.com/osuecampus/geolocation-recording-application/blob/master/distance.js)

3. Display the name, latitude, longitude and calculated distance for each city in the JSON file.

4. Allow the user to sort the data, ascending and descending, based on the distance.

### Restrictions

Only use Javascript, CSS and HTML. No jQuery, React. Bootstrap, etc should be used.
