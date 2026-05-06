# FreeAPI: Random Users UI

A React + TypeScript application that fetches and displays random user profiles from the [FreeAPI](https://freeapi.app) public API with pagination support.

## Live Preview

![alt text](<Screenshot (270).png>)
---

## Features

- **Pagination** — Browse through 500 users with Prev/Next controls
- **Rich Profile Cards** — Each card displays:
  - Profile photo with gradient banner
  - Full name with title
  - Gender & nationality badges
  - Age and membership duration stats
  - Username
  - Email address
  - Phone number
  - Full street address with city, state, country
  - Registration date
- **Professional UI** — Clean blue/white color scheme
- **Responsive Grid** — Auto-fills columns based on screen width (min 280px)
- **Smooth Interactions** — Card hover lift effect, loading spinner
- **Error Handling** — Graceful error states

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| React 19 | UI library |
| TypeScript | Type safety |
| Vite | Build tool & dev server |
| CSS (vanilla) | Styling with blue/white theme |
| Inter Font | Typography (Google Fonts) |

---

## API

**Endpoint:**
```
GET https://api.freeapi.app/api/v1/public/randomusers?page={page}&limit={limit}
```

**Query Parameters:**
- `page` — Page number (1-50)
- `limit` — Items per page (default: 10)

**Response shape:**
```json
{
  "statusCode": 200,
  "data": {
    "page": 1,
    "limit": 10,
    "totalPages": 50,
    "previousPage": false,
    "nextPage": true,
    "totalItems": 500,
    "data": [
      {
        "id": 1,
        "gender": "male",
        "name": { "title": "Mr", "first": "John", "last": "Doe" },
        "location": {
          "street": { "number": 123, "name": "Main St" },
          "city": "...",
          "state": "...",
          "country": "..."
        },
        "email": "john.doe@example.com",
        "login": { "username": "johndoe123" },
        "dob": { "age": 35 },
        "registered": { "age": 5 },
        "phone": "...",
        "picture": { "large": "https://..." },
        "nat": "US"
      }
    ]
  },
  "message": "Random users fetched successfully",
  "success": true
}
```

**Fields Used:**
- `id` — Unique identifier
- `name` — Title, first, last name
- `gender` — Male/female
- `location.street` — Street number & name
- `location.city`, `state`, `country` — Full address
- `email` — Email address
- `phone` — Phone number
- `login.username` — Username
- `dob.age` — User age
- `registered.age` — Years since registration
- `picture.large` — Profile photo URL
- `nat` — Nationality code

---

## Getting Started

### Prerequisites

- Node.js >= 18
- npm

### Installation

```bash
# Clone the repo
git clone <your-repo-url>
cd freeapi-random-users-ui

# Install dependencies
npm install

# Start dev server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
npm run preview
```

---

## Project Structure

```
src/
├── App.tsx       # Main component — API fetch, pagination, card rendering
├── App.css       # Card styles, grid layout, blue/white theme
├── index.css     # Global reset & Inter font import
└── main.tsx      # React entry point
```

---

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |




