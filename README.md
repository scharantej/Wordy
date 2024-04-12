## Flask Application Design

### Problem Statement

Provide a Flask application that allows users to submit a query and receive a response based on the query. The queries should be stored in a database for future reference.

### HTML Files

- **index.html**
   - Contains the form for users to submit their queries.
   - Includes an input field for the query, a submit button, and a display area for the response.

### Routes

- **/submit**
   - **Method:** POST
   - **Purpose:** Receives the submitted query and saves it to the database.
   - **Functionality:**
     - Parses the form data and extracts the query.
     - Connects to the database and inserts the query into a table.
     - Redirects to a confirmation page with a success message.

- **/query**
   - **Method:** GET
   - **Purpose:** Retrieves the queries from the database and displays them in the confirmation page.
   - **Functionality:**
     - Connects to the database and retrieves all queries.
     - Renders a page showing the list of queries.

- **/response**
   - **Method:** POST
   - **Purpose:** Responds to a specific query based on the user's input.
   - **Functionality:**
     - Parses the form data and extracts the query ID.
     - Connects to the database and fetches the response for the corresponding query.
     - Renders a page displaying the response.