# ghostly
Ghostly is a void that let's you speak into it :)


## UI mockups

[figma mockup](https://www.figma.com/proto/NxbNHLwdU2xYvnavkfeYER/Ghostly?node-id=214%3A366&scaling=min-zoom&page-id=123%3A1)


## Schema design


![ghostly_schema](https://user-images.githubusercontent.com/20106622/116774465-66102c00-aa7a-11eb-93b4-77f8aac28a4e.PNG)



- Note: I'm considering the system to have millions of likes and replies so making the database trade-off accordingly.


## APIs

**login**
----
  Login into the void with user_name and password.

* **URL**

  api/auth/login/v1

* **Method:**

  `POST`
  
*  **URL Params**

   **Required:**
 
   None

* **Data Params**

   **Required:**
 
   - `user_name`
   - `password`

* **Success Response:**

  * **Code:** 201 <br />
    **Content:** `{ token : "Bearer jwt_token_string", message:'Login success!' }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "Invalid user name or password" }`

* **Sample Call:**

  ```javascript
  curl --location --request POST 'ghostify.com/api/auth/login/v1' \
  --header 'Content-Type: application/json' \
  --data-raw '{

      "user_name":"@aamir2void",
      "password": "*****"
  }'
  ```
