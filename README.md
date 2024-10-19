# GithubFinder
The provided code is an HTML document that serves as a simple "GitHub Finder" webpage. This webpage allows users to search for GitHub profiles using the GitHub API and displays the search results. Below is a detailed breakdown of each part:

1. **HTML Structure:**
           Document Type: It uses the **<!DOCTYPE html>** declaration for HTML5.
           <html lang="en">: The document is set in English.
           <head> Section:
**It includes the following:**
          Meta tags for character encoding (UTF-8), compatibility with Internet Explorer (IE=edge), and responsiveness (viewport).
          Bootstrap CSS for styling and responsive design using the Bootstrap 5 framework.
          Font Awesome for including GitHub brand icons (e.g., the GitHub logo).
          A custom <style> tag for additional styling.
          Page title: "Github Finder | Home Page".
**2. CSS Styling**:
          The custom CSS styles within the <style> block define the overall appearance:
          Body: Dark background with white text.
          Inputs and buttons: Styled with custom width, height, padding, and border-radius to give them a sleek, minimal look.
          Images: Set to appear as small circular avatars.
          Links: Styled with a white color and an opacity effect when hovered.
**3. Navbar:**
          A navigation bar is created using Bootstrap components:
          It features a GitHub logo (Font Awesome icon) and text (Github Finder).
          Links: Two navigation links are present:
          "HOME" link (though it doesn't link anywhere).
          "ABOUT" link, which opens an external portfolio page in a new tab.
**4. Main Search Section:**
          The main container is structured using Bootstrap's grid system.
          Inside the first column:
          A message: "Let's stalk someone on Github".
          An input field where users can enter a GitHub username, and a search button labeled "GO".
          The input and button are styled to appear side by side using flexbox.
**5. Results Section:**
          Another container uses Bootstrap's grid layout to display the search results dynamically, which is updated by JavaScript based on the user's search.
**6. JavaScript Functionality:**
         The JavaScript code is responsible for handling user interactions and fetching data from the GitHub API:
**getData() Function:**
         It is triggered when the user clicks the "GO" button.
**Input validation: **It checks if the user has entered a GitHub username. If not, it alerts the user.
         It sends an API request to GitHub's search endpoint using fetch based on the entered username.
         The response is converted to JSON format.
         For each result (user profile), the function generates dynamic HTML and displays the user's:
         Avatar (profile picture).
         Username and a link to their GitHub profile.
**fninputText() Function:**
         It handles clearing the results when the input field is empty.
**7. API Integration:**
        The app uses GitHub's user search API to fetch profiles based on the inputted username.
   The API URL used is:
   plaintext
   Copy code
   https://api.github.com/search/users?q=${originalName}&page,per_page,sort,order
   The data returned includes user information such as:
    Login: The username of the profile.
   Avatar URL: The user's profile picture.
   HTML URL: The link to the user's GitHub profile.
**8. Dependencies:**
    Bootstrap (v5.0.2): For layout and styling.
    Font Awesome: For icons (GitHub icon in this case).
    GitHub API: For fetching user profiles.
**Summary:**
This is a small web app that provides a UI for searching GitHub users. When a username is entered, the app fetches the user's details using the GitHub API and displays their avatar, username, and profile link. The interface is responsive thanks to Bootstrap, and JavaScript powers the search functionality.
