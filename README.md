# eBookSmith

**eBookSmith** is a full-stack web application that uses AI to generate original short stories and package them into downloadable eBooks. Users can enter a creative prompt, refine AI-generated content, upload a custom cover image, and export the result as a valid EPUB file. The application also maintains a local library of generated works for browsing and review.

This project was built as a collaborative course project with a focus on clean UI design, practical backend architecture, and real-world web technologies.

---

## Features

* **AI-Generated Story Content**

  * Generate original story drafts from a user prompt
  * Auto-generate titles
  * Fully editable story text before export

* **EPUB eBook Generation**

  * Converts generated content into valid EPUB format
  * Supports custom author name and cover image upload
  * Produces clean XHTML-compliant eBook files

* **Library & Activity Tracking**

  * Logs generated eBooks locally using SQLite
  * Displays generation history in a searchable, sortable table
  * Tracks title, author, endpoint used, and timestamp

* **Modern UI & UX**

  * Responsive design using Bootstrap 5
  * Shared dynamic navbar and footer
  * Particle fire animation background for visual polish
  * Carousel landing page and FAQ system

---

## Tech Stack

### Frontend

* HTML5 / CSS3
* JavaScript (ES6)
* Bootstrap 5
* jQuery
* DataTables
* tsParticles (fire preset)

### Backend

* PHP
* SQLite (local logging)
* REST-style PHP endpoints

### AI Integration

* ChatGPT API (for title and story generation)

---

## Project Structure

```
/
├── index.html              # Landing page
├── forge.html              # Story & eBook generation UI
├── activity.html           # Library / history view
├── help.html               # FAQ & help content
├── dylanKendall.html       # Developer profile
├── tanishaSikder.html      # Developer profile
│
├── css/
│   └── style.css           # Global site styling
│
├── js/
│   ├── forge.js            # Forge page logic
│   ├── getActivity.js      # Library table population
│   ├── fireParticles.js    # Background animation
│   └── loadCommonElements.js
│
├── php/
│   ├── generateContent.php # AI story generation
│   ├── generateTitle.php   # AI title generation
│   ├── generateEBook.php   # EPUB creation logic
│   ├── logTransactions.php # SQLite logging
│   └── RestServer.php      # Backend routing/utilities
│
├── assets/
│   ├── images, videos, logos
│
└── database/
    └── SQLite database file
```

---

## How It Works

1. The user enters a story prompt on the **Forge** page.
2. A PHP backend endpoint sends the prompt to the ChatGPT API.
3. The AI returns generated story content and/or a title.
4. The user can edit the story, add author info, and upload a cover image.
5. On submission, the backend:

   * Formats the content into valid XHTML
   * Packages everything into an EPUB
   * Logs the transaction to SQLite
6. The generated eBook is returned to the user for download.
7. The **Library** page displays all logged generations.

---

## Running Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/ebooksmith.git
   ```

2. Run the project using a local PHP server:

   ```bash
   php -S localhost:8000
   ```

3. Open your browser:

   ```
   http://localhost:8000/index.html
   ```

> **Note:** An API key is required for AI generation. Configure this securely in the PHP backend (not included in the repo).

---

## Team & Contributions

### Dylan Kendall

* Backend & full-stack development
* AI integration (ChatGPT)
* EPUB generation logic
* SQLite transaction logging
* Forge & Library page implementation
* Global UI theming and component system

### Tanisha Sikder

* Frontend development
* UI/UX design and layout
* Carousel, FAQ, help system
* Media creation and visual content
* HTML/CSS structure and styling

---

## What This Project Demonstrates

* Practical full-stack web development
* Clean separation of frontend and backend responsibilities
* Real-world AI API integration
* File generation and format compliance (EPUB/XHTML)
* Thoughtful UI design and user experience polish

---

## License

This project is provided for educational purposes.
Feel free to explore, modify, and learn from the code.
