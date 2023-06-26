
# **Recipe API Search App built with Vue3, Vite & Tailwind CSS** 

This app utilizes a Meal Database API and allows the user to search recipes through various methods.

**Project Development Process**

**Initial ideas:**
My partner and I love to cook and are always saving recipes for each other.  A caveat of this is we find them from different sources (pinterest, instagram, etc) so it can be hard to keep track of where the recipes originated when trying to recall.   A solution my partner had for this is an all-in-one recipe “hub” app that would be able to search recipes from any cooking-based site. When this opportunity was presented to integrate an API I knew this was the idea to run with!  

**Development Process:** First I set out to find a free database containing recipes and found this one: https://www.themealdb.com/api.php 
From there, I decided which endpoints I wanted as my core functionality.  So for this project I set the base mvp to have the user be able to: search meals by the name, by first letter of the recipe name, and by ingredients in the recipe.  This core functionality would allow users to vary their methods for finding recipes and create a somewhat “customized” approach to finding dishes as opposed to providing only one option for searching (an aspect my partner would appreciate 🙂).  Once I implemented the “search meals by name” page successfully, that served as my core logic for continuing the iterative development process by utilizing modular components (for ex. one singular meal item), using my store dispatch actions and passing props with relative search logic in each page.  

**Design Rationale:**
For the sake of building a relatively simple, modern looking site, I utilized tailwind css since I find it to be very easy for styling and can work quickly to implement small changes on the fly.  It’s also easy to further develop over time as I have memorized most of the property codes.  I do plan to continue to develop the color scheme past this deadline but for now I think the simple design is effective enough and doesn’t detract from the “star” of the site which is the recipe API.

**Testing Strategies:** For testing purposes I utilized the debugger to ensure that I was sending/receiving data even if I wasn’t seeing anything in the browser.  This was helpful for my testing my onMounted functions and for checking that the correct objects were being returned for the relative search logic (for ex. data with a recipe name starting with “L” is being returned in the response).  I also had my partner use the site for Usability testing purposes and she found the site intuitive and easy to navigate.

**Challenges/Solutions:** Challenges I faced with this project were in the little details such as checking that I was passing props correctly, making sure that I was nesting components in the correct hierarchy,  and being able to solve any console errors (“module not found”, “blank__ is not a function”, etc).  As much as I love when things are working correctly, I absolutely love when I get the chance to find and solve an error - it’s extremely rewarding and helps build confidence that I have the knowledge and grit to remedy any error thrown at me.   Another challenge I faced was in deployment: Vercel didn’t like that I was setting Vuejs as the framework so it kept failing until I selected “Other” as the framework and it deployed successfully!

