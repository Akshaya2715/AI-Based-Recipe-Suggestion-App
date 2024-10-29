# AI-Based-Recipe-Suggestion-App
AI-Based Recipe Suggestion App using Java
The AI-Based Recipe Suggestion App is a Java-based application that generates recipe ideas based on user-provided ingredients. Using the Google Gemini API, it retrieves customized recipe suggestions and stores them in an embedded Apache Derby database, making it easy for users to explore culinary ideas interactively.

Key Technologies Used
Java: Core programming language for building and managing the application logic.
Apache Derby: Lightweight, embeddable database for storing user inputs and recipe suggestions, enabling offline data access.
Google Gemini API: API to generate personalized recipe suggestions based on provided ingredients.
Swing: Java library for creating an intuitive graphical user interface (GUI).
OkHttp: A Java library to handle HTTP requests to the Google Gemini API.
JSON: Data format for structuring and exchanging information between the API and the application.
Application Workflow
User Input:

User enters a list of ingredients in a designated text area within the app.
Submit Action:

When the "Get Recipe Suggestions" button is clicked, the app initiates the recipe suggestion process.
Validation:

Before making an API request, the app verifies that the input is not empty. If empty, it displays a prompt for the user to enter ingredients; otherwise, it continues to the next step.
API Request:

A JSON payload is created with the ingredients list. Using OkHttp, the app sends a POST request to the Google Gemini API for personalized recipe suggestions.
API Response Handling:

Upon receiving the API response, the app checks for success. If successful, it extracts the recipe suggestions. If unsuccessful, it displays an appropriate error message to the user.
Display Suggestions:

Recipe suggestions are displayed in a response area for easy viewing by the user.
Save to Database:

The entered ingredients and suggested recipes are stored in an Apache Derby database, allowing users to review previous suggestions even without an active internet connection.
Clear Action:

If the user clicks the "Clear" button, both the input and response areas are reset for a new entry.
