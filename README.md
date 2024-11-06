# StudyGo API Documentation

**Base URL:** `https://api.wrts.nl/api/v3`

## Endpoints

### 1. **Authentication**
- **Endpoint:** `/auth/get_token`
- **Description:** Authenticates a user and returns a token.
- **Method:** POST
- **Payload Parameters:**
  - `email` (string, required): The user's email address.
  - `password` (string, required): The user's password.
  - `recaptcha_token` (string, optional): Required only if the server responds with a `429` status, indicating CAPTCHA validation is needed.
- **Headers:** None required initially.

### 2. **User Data**
- **Endpoint:** `/get_user_data`
- **Description:** Retrieves a JSON object with user information.
- **Headers:** 
  - `x-auth-token` (string, required)

### 3. **Suggested Subjects**
- **Endpoint:** `/subjects/suggested_subjects`
- **Description:** Returns a JSON object containing suggested subjects for the user.
- **Headers:** 
  - `x-auth-token` (string, required)
