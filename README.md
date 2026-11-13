# LearnHub LMS — GitHub Pages Prototype

A responsive front-end Learning Management System built with **HTML, CSS, and vanilla JavaScript**.

## Features
- Dashboard with student, course, attendance, and grade summaries
- Student records: add, search, and delete
- Course catalog: add and delete courses
- Attendance: mark Present, Absent, or Late by date
- Grades: record scores from 0–100 and view remarks
- Browser storage using `localStorage`
- Responsive layout for desktop and mobile

## Run locally
1. Download or extract the project ZIP.
2. Open `index.html` in a modern web browser.

## Publish using GitHub Pages
1. Create or open your GitHub repository.
2. Upload `index.html`, `style.css`, `script.js`, and `README.md` to the repository's root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then click **Save**.
6. Wait for GitHub Pages to publish, then open the website link shown in the Pages section.

## Important project limitation
This is a **front-end academic prototype**. `localStorage` saves data only in the current browser on the current device. Records are not shared with other users or devices. There is no real authentication, server, or cloud database, so do not enter private or sensitive student information.

For a production LMS, connect the interface to a secure backend/API and database, and implement proper authentication and access controls.

## Suggested project architecture
- **Presentation layer:** `index.html` and `style.css` render the interface.
- **Application layer:** `script.js` handles navigation, validation, module actions, and data updates.
- **Storage layer:** browser `localStorage` stores the prototype data.

### Data flow
A user submits a form or changes attendance → JavaScript validates the input → the relevant data collection is updated → `localStorage` saves the updated data → the dashboard and module tables re-render.

## Suggested ERD entities
- **Student** (`student_id` PK, `full_name`, `email`, `program`)
- **Course** (`course_code` PK, `course_title`, `description`, `instructor`)
- **Attendance** (`attendance_id` PK, `student_id` FK, `attendance_date`, `status`)
- **Grade** (`grade_id` PK, `student_id` FK, `course_code` FK, `score`)

The browser prototype uses simple arrays/objects for demonstration. The ERD above is a suggested relational design for the documentation.
