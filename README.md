# StudyGo API Documentation

**Base URL:** `https://api.wrts.nl/api/v3`

## Endpoints

### 1. **Authentication**
- **Endpoint:** `/auth/get_token`
- **Method:** POST
- **Description:** Authenticates a user and returns a JSON object with a session token (this token will be the `x-auth-token` header).
- **Parameters:**
  - `email` (string, required)
  - `password` (string, required)
  - `recaptcha_token` (string, optional, used on `429` errors)

### 2. **User Data**
- **Endpoint:** `/get_user_data`
- **Method:** GET
- **Description:** Returns a JSON object with user profile details (e.g., name, email, preferences).
- **Headers:** `x-auth-token`

### 3. **Suggested Subjects**
- **Endpoint:** `/subjects/suggested_subjects`
- **Method:** GET
- **Description:** Returns a JSON object listing suggested subjects for the user.
- **Headers:** `x-auth-token`

### 4. **items_overview**
- **Endpoint:** `/items_overview`
- **Method:** GET
- **Description:** Returns a JSON object with your recent excercises
- **Headers:** `x-auth-token`
