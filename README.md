# Blog API

This project is a **Flask-based Blog API** that allows users to retrieve and manage blog posts. It supports functionalities such as sorting blog posts by various fields and directions and comes with an all-inclusive structure for testing the API functionalities.

---

## Features

- **Retrieve Blog Posts:**
  - API to fetch all blog posts, optionally supporting sorting.
- **Sorting:**
  - Sort posts by `title` or `content` in **ascending** or **descending** order.
- **Flask Framework:**
  - Backend powered by Flask for simplicity and extensibility.
- **Testing with Pytest:**
  - Tests to ensure sorting functionality works correctly.

---

## File Structure

- `backend/`
  - **Contains the main Flask application.**
- `tests/`
  - **Includes test files to verify the functionality of the API using `pytest`.**
- `POSTS`:
  - **A sample dataset of blog posts, imported and used in API endpoints and tests.**

---

## How It Works

1. **API Endpoints:**
   - Primary endpoint: `/api/posts`
   - Query Parameters:
     - `sort` — Field to sort by (e.g., `title` or `content`).
     - `direction` — Sorting direction (`asc` or `desc`, defaults to `asc`).

2. **Sorting Logic:**
   - Blog posts can be sorted based on the title or content field.
   - Supports ascending and descending order sorting.

3. **Sample Sorting Use Cases:**
   - Fetch posts, sorting by `title` (ascending):
     ```
     GET /api/posts?sort=title
     ```
   - Fetch posts, sorting by `content` (descending):
     ```
     GET /api/posts?sort=content&direction=desc
     ```

4. **Tests:**
   - The project is equipped with test cases using `pytest` to validate:
     - Sorting results by title (ascending and descending).
     - Sorting results by content (ascending and descending).
   - Tests directly work with the `/api/posts` endpoint to verify the proper JSON response and ordering.

---

## Installation & Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd blog
   ```

2. Set up a virtual environment (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Linux/macOS
   venv\Scripts\activate     # On Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   flask run
   ```

5. Run the tests:
   ```bash
   pytest
   ```

---

## Testing

This project includes robust test cases using `pytest`, which ensures the correctness of sorting functionality.

### Example Test Cases

- **Sort by Title (Ascending and Descending):**
  - Tests that titles are sorted alphabetically in ascending or descending order.
- **Sort by Content (Ascending and Descending):**
  - Tests that the content of blog posts is sorted correctly.

Run the tests via:
```bash
pytest
```

All test cases will validate that the API is functioning as intended.

---

## Dependencies

The project relies on the following Python packages:

- **Flask**: Backend framework for serving the APIs.
- **Flask-SQLAlchemy**: Provides database integration if needed for future enhancements.
- **Pytest**: Framework used to write the test cases.
- **Werkzeug**: Used internally by Flask for utilities.
- **Requests**: Simplifies API testing (optional).
- **Jinja2**: For templating if required for API extensions.

Install all dependencies from the `requirements.txt` file.

---

## Contribution

Contributions, issues, and feature requests are welcome! Feel free to fork and submit a PR for improvements or bug fixes.

- Fork the repository
- Create a new branch (`feature/your-feature`)
- Commit your changes
- Open a pull request

---

## License

This project is licensed under the MIT License. 

Feel free to use and extend the project for personal or commercial purposes.
