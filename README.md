# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - Recipe page solution](#frontend-mentor---recipe-page-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [Documentation](#documentation)
    - [Requirements](#requirements)
      - [Functional Requirements](#functional-requirements)
        - [Frontend](#frontend)
        - [Backend](#backend)
      - [Non-Functional Requirements](#non-functional-requirements)
      - [Bonus Features (Optional)](#bonus-features-optional)
    - [API Design](#api-design)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## Documentation

### Requirements

#### Functional Requirements

##### Frontend

1. Homepage:
   - Display a list of featured recipes
   - Include a navigation bar with links to:
     - Home
     - Recipe Categories (e.g., Breakfast, Desserts, Main Courses)
     - Search Page
   - Show a "Load More" button to fetch additional recipes dynamically
2. Recipe Details Page:
   - Fecth and display a specific recipe when a user clicks on it
   - Display recipe information:
     - Title
     - Image
     - Description
     - Ingredients (list format)
     - Steps/Instructions (ordered list format)
     - Cooking time, preparing time, and total time
     - Nutrition information (calories, protein, carbs, fat)
   - Allow users to navigate back to the homepage or search Page
3. Search and Filter Page:
   - Provide a search bar for keyword-based searching (e.g., Chicken)
   - Include filters:
     - Cuisine Type (e.g., Italian, Indian)
     - Difficulty Level (e.g., Easy, Medium, Hard)
     - Ingredients (multi-select dropdown)
   - Dynamically render search results as users type or adjust filters.
4. Responsive Design:
   - Ensure the app is mobile-friendly and adjusts appropriately on different screen sizes.
5. User Interactions:
   - Allow users to mark recipes as "Favorites" (bonus: persist this data with local storage or user accounts)
   - Allow sharing recipes via social media or copying a link

##### Backend

1. Recipe Database:
   - Store recipe information with fields:
     - ID, Title, Description, Image URL.
     - Preparing Time, Cooking Time, Total Time.
     - Ingredients (stored as an array)
     - Instructions (stored as an array of steps).
     - Nutrition Information (calories, protein, carbs, fat).
     - Tags (e.g., cuisines, difficulty level).
     - Created/Updated Timestamps
2. API Endpoints:
   - GET /recipes:
     - Fetch all recipes with pagination support (?page=1&limit=10)
   - GET /recipes/:id:
     - Fetch a specific recipe by ID
   - POST /recipes:
     - Add a new recipe (admin-only access).
   - PUT /recipes/:id
     - Update an existing recipe (admin-only access).
   - DELETE /recipes/:id
     - Delete a recipe (admin-only access).
   - GET /recipes/search:
     - Search recipes based on keywords (?q=chicken) and filter criteria (?cuisine=italian&difficulty=easy).
3. Search and Filtering:
   - Use database queries to filter recipes by:
     - Cuisine
     - Difficulty Level
     - Ingredients (match any/all)
   - Implement ful-text search (if using MongoDB, use $text; if MySQL, use FULLTEXT)
4. Authentication (optional)
   - Allow admin users to manage recipes (CRUD)
   - Use JWT for securing API endpoints

#### Non-Functional Requirements

1. Performance:
   - Implement caching (e.g., Redis) to speed up repeated requests for recipe data and search results
   - Optimize database queries for large datasets
2. Scalability:
   - Structure the backend to support additional features like user accounts, comments, or ratings in the future
3. Security:
   - Validate and sanitize all user inputs to prevent SQL Injection, XSS, etc.
   - Use HTTPS for secure communication
4. Error Handling:
   - Return meaningful error messages for failed API calls (e.g, 404 for "Recipe Not Found").
   - Implement a fallback UI on the frontend for failed data fetching.
5. Accesibility:
   - Ensure the frontend is keyboard-navigable and screen reader-friendly.
6. Documentation:
   - Provide API documentation (e.g., Swagger/OpenAPI) for all endpoints.
   - Write a README file explaining the project structure, setup instructions, and usage

#### Bonus Features (Optional)

1. User Accounts:
   - Allow users to create an account, save favorite recipes, and submit their own recipes.
2. Recipe Ratings and Reviews:
   - Enable users to leave reviews and rate recipes.
3. Image Upload:
   - Allow users or admins to upliad recupe images (use Cloudinary or local storage)
4. Notifications:
   - Notify users when new recipes are added or if a recipe matches their saved preferences.

### API Design

## My process

### Built with

- React
- Node.js
- Express
- Docker
- Postgresql
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```

```css
.proud-of-this-css {
  color: papayawhip;
}
```

```js
const proudOfThisFunc = () => {
  console.log('🎉');
};
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Frontend Mentor - [@papitapapita](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@papitapapita](https://www.twitter.com/yourusername)
- LinkedIn - [Jonathan Olivos](https://www.linkedin.com/in/jonathan-olivos-400950187/)

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
