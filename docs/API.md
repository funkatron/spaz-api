Meta
=====
         API Documentation, generated 2010-11-15T10:10:18+00:00
         Actions      : 4
         Errors       : 6
         Output Types : 5


Actions
================================================================================


get_ip
------------------------------------------
### Description

 returns the public IP from the requesting machine

### URL 

* /ip


### No parameters associated to this action
        
        
    

get_url_info
------------------------------------------
### Description

 preview the contents of a URL in some way

### URL 

* /url/info

### Parameters
                
* url		(**Required**)
                
        
    

get_url_title
------------------------------------------
### Description

 Retrieves the Title of an HTML doc located at the URL, or the content type if not text/html

### URL 

* /url/title

### Parameters
                
* url		(**Required**)
                
        
    

retrieve
------------------------------------------
### Description

 Retrieve information about a certain URL

### URL 

* /url/retrieve

### Parameters
                
* url		(**Required**)
                
        
    

Errors
=======


ERROR_GET_EXPECTED
----------------------------

### HTTP Response Code
    400
### Developers Message (Sent back to the developers)
    Only a GET is expected for this API module


### Error Description
    This error is returned whenever a module that only expects an HTTP GET receives anything else.


ERROR_INSERTING_IMAGE
----------------------------

### HTTP Response Code
    400
### Developers Message (Sent back to the developers)
    There was an unexpected error while inserting the new image in the cache


### Error Description
    This error is returned when something wrong happened when saving to the couchdb database.


ERROR_INVALID_URL
----------------------------

### HTTP Response Code
    400
### Developers Message (Sent back to the developers)
    An invalid URL was submitted


### Error Description
    This error is returned when the URL passed to the webservice is an invalid URL.


ERROR_NO_SUCH_IMAGE
----------------------------

### HTTP Response Code
    404
### Developers Message (Sent back to the developers)
    No image found for that URL


### Error Description
    This message is returned when no image was matched in the retrieval process.


ERROR_RATE_LIMIT_EXCEEDED
----------------------------

### HTTP Response Code
    401
### Developers Message (Sent back to the developers)
    You are only authorized to create a new thumbnail every minute. You currently hit the rate limit and this will go away in 60 seconds.


### Error Description
    This error is returned when someone tries to access a new thumbnail in less than 1 minute within the rate limit.


NO_THUMB_FOR_THAT_URL
----------------------------

### HTTP Response Code
    400
### Developers Message (Sent back to the developers)
    There was an error while making a thumbnail out of the supplied URL.


### Error Description
    This error is returned when no image has been supplied back for that URL.

Output Types
==============
* CLI 		(**Enabled**)		

* PHP 		(**Enabled**)		

* XML 		(**Enabled**)		

* JSON		(**Enabled**)		and this one is the **Default** output type

* PRINTR		(**Enabled**)		


Frapi, echolibre ltd.
======================
