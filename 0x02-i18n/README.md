# i18n Project

This project focuses on learning how to create internationalized web pages using Flask.

## Tasks Overview

### 0. Basic Flask App
- **File**: [0-app.py](0-app.py)
- **Task**: Set up a Flask app with a single `/` route and an [index.html](templates/0-index.html) template. The page should display "Welcome to Holberton" as the title (`<title>`) and "Hello world" as the header (`<h1>`).

### 1. Basic Babel Setup
- **Files**: [1-app.py](1-app.py), [templates/1-index.html](templates/1-index.html)
- **Steps**:
  1. Install Flask-Babel:
     ```bash
     pip3 install flask_babel
     ```
  2. Create a `Babel` object and configure supported languages `["en", "fr"]`.
  3. Set default locale (`"en"`) and timezone (`"UTC"`) using a `Config` class.

### 2. Get Locale from Request
- **Files**: [2-app.py](2-app.py), [templates/2-index.html](templates/2-index.html)
- **Task**: Implement a `get_locale` function to select the best match for supported languages using `request.accept_languages`.

### 3. Parametrize Templates
- **Files**: [3-app.py](3-app.py), [templates/3-index.html](templates/3-index.html)
- **Task**:
  1. Use `_` or `gettext` to parametrize messages like `home_title` and `home_header`.
  2. Create a `babel.cfg` file for translation extraction.
  3. Initialize and compile language dictionaries for `en` and `fr`.

### 4. Force Locale with URL Parameter
- **Files**: [4-app.py](4-app.py), [templates/4-index.html](templates/4-index.html)
- **Task**: Modify `get_locale` to detect `locale` in the URL parameters and return the matching locale.

### 5. Mock Logging In
- **Files**: [5-app.py](5-app.py), [templates/5-index.html](templates/5-index.html)
- **Task**: Emulate a user login system using a URL query parameter (`login_as`) and display a welcome message for logged-in users.

### 6. Use User Locale
- **Files**: [6-app.py](6-app.py), [templates/6-index.html](templates/6-index.html)
- **Task**: Update `get_locale` to prioritize locale selection in this order: URL, user settings, request headers, default.

### 7. Infer Time Zone
- **Files**: [7-app.py](7-app.py), [templates/7-index.html](templates/7-index.html)
- **Task**: Implement `get_timezone` to select the time zone based on URL parameters, user settings, or default to UTC. Validate using `pytz`.

### 8. Display Current Time
- **Files**: [app.py](app.py), [templates/index.html](templates/index.html)
- **Task**: Display the current time in the inferred time zone on the home page, using translated messages for both English and French.

## Resources
- [Flask-Babel Documentation](https://intranet.alxswe.com/rltoken/fBpGjDt2BFuBFiz-jwublQ)
- [Flask i18n Tutorial](https://intranet.alxswe.com/rltoken/RtGz7pI7TKnYqrMMG9rWMg)
- [pytz Documentation](https://intranet.alxswe.com/rltoken/7rrCz4pkpqAn4FfRZ2Vsvw)