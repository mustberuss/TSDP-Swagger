# TSDR-Swagger
Improvements to the USPTO's Swagger object for its TSDR api

I made the following changes to their swagger object 
- The USPTO-API-KEY:api key is sent as a header on all calls
- Parameters were added to /casedocs/bundle.xml, /casedocs/bundle.pdf and /casedocs/bundle.zip endpoints
- "type" was added an enum in /caseMultiStatus/{type} and its description was updated.
- "schemes": ["https"] was added
- The trailing / on basePath was removed, making it "/ts/cd"
- The image endpoint /rawImage/{serial_number} was added
- 401's and 429's were added as possible api returns on all endpoints
- Additional parameters were added to the /casedocs/bundle.pdf and /casedocs/bundle.xml endpoints
- The tags on /casedocs/bundle.xml,/casedocs/bundle.pdf and /casedocs/bundle.zip were changed from "Resource for retrieving multiple documents of a single case" to "Resource for retrieving data for multiple cases".

## Links
- My Swagger-UI pages using the updated swagger object
    + https://mustberuss.github.io/TSDR-Swagger/ Swagger 2
    + https://mustberuss.github.io/TSDR-Swagger/openapi.html OpenAPI/Swagger 3 
- USPTO links
    + https://developer.uspto.gov/api-catalog/tsdr-data-api Information on the api
    + https://developer.uspto.gov/swagger/tsdr-api-v1 Swagger-UI page

**Notice:** The TSDR api does not currently allow browser request (CORS issues) so requests from this page will not actually work. The generated curl commands will work and the modified swagger object can be imported into postman.
