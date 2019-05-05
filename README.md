
# Geolocation Recording Application

## Summary

An instructor has asked our team to develop an application that can record the name and coordinates of places that students will be visiting throughout the world. 

Our team has agreed that it can deliver a simple geolocation recording application for this Ecampus course. It will be a web application that runs on all major browsers and modern mobile devices.

**Restrictions**
Due to potential conflicts with the course management system, we cannot use jQuery, React, or any other javascript library. 


## Intended Use

Students will get the geolocation (latitude and longitude) of a location through a separate tool. They will be expected to input the the name of the location, the latitude, and the longitude into the recording application.

The data they enter will be submitted by the recording application to a backend database, via an API already provided (details below).

Students should be able to view any information about their recorded locations using the recording application.

## Requirements

### Features 

As a user, I would like to add a new location.
As a user, I want to see a list of all locations (no sorting necessary).
As a user, I want to see the name and coordinates (latitude, longitude) of each location.
As a user, I want my records saved to the Datastore so they persist beyond a single session.

### Data Validation

Latitude should be with a range of -90 to 90.
Longitude should be within a range of -180 to 180.
Latitude and longitude should not accept any non-numerical characters.

### Accessibility

As a user, I should be able to focus on each input using tab.
As a user, I should be able to complete the exercise using only the keyboard.

## Optional

As a user, I want to edit a location.
As a user, I want to delete a location.


## Data Architecture

### Location

A location should contain the name and coordinates (latitude and longitude). How these are recorded and displayed are not important.

### Formatting

Use [JSON.stringify()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify) to turn the location values into a string which can be used for creating a new item with the Datastore API.

Use [JSON.parse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) to transform the API response from a string to an object.


## Datastore

### Base URL

https://demo-api.oregonstate.education/api/

### API

#### Create Item (POST)
*base_url*/item

**Request Parameters**
*user_id* - string - Your user ID (made up).
*value* - string

#### Get Items (GET)
*base_url*/items

**Request Parameters**
*user_id* - string - Your user ID (made up).




#### Update Item (PUT)
*base_url*/item

**Request Parameters**
*user_id* - string - Your user ID (made up).
*id* - integer - ID of the item you want to update.
*value* - string - New string to replace the previous value with.


#### Delete Item (DELETE)
*base_url*/item

**Request Parameters**
*user_id* - string - Your user ID (made up).
*id* - integer - ID of the item you want to delete

### Insomnia

You can use Insomnia to make the REST calls during development. This application is similar to Postman or Paw. It is not required, but available for additional assistance in understanding the API.

[https://insomnia.rest/](https://insomnia.rest/)
[Document]


### Data Store Sample Item

```
{
      "id": "4",
      "user_id": "100",
      "value": "5",
      "created_date": "1556932540",
      "edit_date": null
}
```

**id** (integer, read-only)  is the unique identification number for this item.
**user_id** (string)  is the name of user who created the item.
**value** (string) is contents of the item.
**created_date** (integer, read-only) is a Unix timestamp from when the item was created.
**edit_date** (integer, read-only) is a Unix timestamp from when the item was edited (if it was) (read only)
