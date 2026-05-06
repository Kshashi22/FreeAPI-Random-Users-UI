
# FreeAPI: Random Users UI

A web application that fetches and displays random user data from a free public API. This project demonstrates API integration, asynchronous JavaScript, and dynamic UI rendering.

---

## Features

* Fetch random user data from a public API
* Display user details such as name, email, location, and profile picture
* Generate new users on demand
* Responsive and user-friendly interface
* Fast and lightweight application

---

## Tech Stack

* Frontend: HTML, CSS, JavaScript
* API: Random User API
* Tools: VS Code, Git, Browser DevTools

---

## Project Structure

```
FreeAPI-Random-Users-UI/
│── index.html
│── style.css
│── script.js
│── README.md
```

---

## Installation and Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/FreeAPI-Random-Users-UI.git
   ```

2. Navigate to the project directory:

   ```bash
   cd FreeAPI-Random-Users-UI
   ```

3. Open the `index.html` file in your browser

---

## API Integration

Example API used:

```
https://randomuser.me/api/
```

### Fetch Example

```javascript
fetch('https://randomuser.me/api/')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

## How It Works

1. The application sends a request to the Random User API
2. The API returns user data in JSON format
3. The application extracts relevant details
4. User information is dynamically displayed on the interface

---

## Data Displayed

* Full Name
* Email Address
* Profile Picture
* Location (City, Country)
* Gender

---

## Future Improvements

* Add multiple user cards display
* Implement search and filtering options
* Add pagination or infinite scrolling
* Save favorite users
* Improve UI/UX with animations and transitions

---

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Submit a pull request



## Acknowledgements

* Random User API for providing free user data
* Open-source community for tools and inspiration

---

If you want, I can also create a combined README for all your FreeAPI projects or convert this into a React or Node.js version.
