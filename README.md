### Objective
Create a small product management application.

### Brief
The purpose of this application is to create an interface for consuming product data from an API.

### Tasks

- The finished application must be able to:
  - Pull a set of products from a persistence layer.
  - List the above products in a UI (in this case, I will implement as REST API).
  - Sort the products by Name, Size, and Category in the UI.
  - Keep the products persisted even after the application has shutdown
  
- Additional?:
  - create product feature.
    - Validate that the Last Purchase Date cannot be less than the creation date
  - delete product feature.
    - Cache the top 5 most recently deleted products
  - update feature.
  - Paginate the list of products by 5, 10, and 20.
  - Add a feature to get the product with the oldest Last Purchased Date from a single category
  - Generate purchase statistics


### Design Notes

The design is based on controller, service and data layer pattern (anti).
The REST API provides access to an Accounts resource.  
An account resource supports
* creating an account
* getting customer accounts
* transferring between accounts
* getting a history of account transfers

Account relationships:
* an account has an account number
* sort code
* and a history of all the transfers it has been involved in


REST API:
* http://localhost:9080/swagger-ui/index.html?configUrl=/v3/api-docs/swagger-config#/
