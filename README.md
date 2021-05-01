# ghostify
Ghostify is a void that let's you speak into it :)

## Schema design

![ghostify](https://user-images.githubusercontent.com/20106622/116771499-98655d80-aa69-11eb-96b1-59acf127f314.PNG)




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
