#Error Codes and the order by which they're returned


Here's the order which the EyeEm API follows to verify requests and the error codes that that might possibly be returned                      
                                          
##Basic Order:
***                                         
                           
* Is the endpoint existing?
    * No: 404 Not Found
    * Yes: Continue.

* Is the method supported by the endpoint?
    * No: 405 Method Not Allowed
    * Yes: Continue.

* Are all required parameters passed in the request?
    * No: 417 Expectation Failed
    * Yes: Continue.

* Is authentication required?
    * Yes: Is the user successfully authenticated?
     * No: 401 Unauthorized
     * Yes: Continue
    * No: Continue.

* Is an App correctly passed in the request? (passed through an access token or a client_id)
    * No: Is the User Authenticated?
        * [No]: 400 Bad Request {"message':"Invalid client."}
        * [Yes]: Skip the App validation mechanism.
    * Yes: Continue.

* Is the App approved?
    * No: 400 Bad Request {"message":"Invalid app (unapproved)."}
    * Yes: Continue

* Is Native scope required for this endpoint?
    * Yes: Is the App native?
        *No: 400 Bad Request {"message':"Insuffisant rights (native access needed)."}
        *Yes: Continue
    * No: Continue

* Is Request a DELETE?
    * Yes: App has 'delete' capabilities?
        * No: 400 Bad Request {"message':"Insuffisant rights (delete access needed)."}
         * Yes: Continue
    * No: Continue

* Is Request a POST or PUT?
    * Yes: App has 'write' capabilities?
          * No: 400 Bad Request
            {"message':"Insuffisant rights (write access needed)."}
          * Yes: Continue
    * No: Continue


##Collections
***
Nothing special for now.
   
#Resource (and sub-resource) endpoints
***
* Is resource (or any of the resource component) existing?
    * No: 404 Not Found {"message":"Photo/User/Album not found."} or {"message":"Unknown Photo/User/Album."}
    * Yes: Continue

* Is the resource private? Or the request PUT/DELETE?
    * Yes: Is the user authenticated?
        * No: 401 Unauthorized {"message':"Unauthorized. Please authenticate."}
        * Yes: Is the authenticated user the resource owner?
    * No: 403 Forbidden
        * Yes: Continue
        * No: Continue


#Status/relation endpoint:
***
* Is the relation possible?
    * No: 404 Not Found {"message":"Photo/User/Album not likeable/followable."}
    * Yes: Continue

* Is the relation existing?
    * No: 404 Not Found {"message":"Photo/User/Album not found."}
    * Yes: Continue


#Then any of the following at any moment:
***
* Is another additional parameter (not in basic required parameters) required to process the request?
    * Yes: 417 Expectation Failed
    * No: Continue.

* Is any of the parameter not valid for any reason?
    * Yes: 400 Bad Request
    * No: Continue.

* Is authentication not required for the endpoint itself, BUT required to process the request (manipulating a resource, accessing a private resource)?
    * Yes: 401 Unauthorized
    * No: Continue.

* Is the user correctly authenticated, BUT not authorized to manipulate/access a resource?
    * Yes: 403 Forbidden
    * N: Continue.

* Is the endpoint/method combination unimplemented at the moment?
    * Yes: 501 Not Implemented
    * No: Continue.
   
* Is the endpoint/method combination not allowed at the moment?
    * Yes: 501 Not Implemented
    * No: ontinue.

* Does the request fail for any other reason?
    * Yes: 500 Internal Server Error
    * No: Continue.
