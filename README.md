# Jac AI Todo App
**Name:**  Mingyang (Dorian) Sun
**UMID:**  19410198

Custom Feature: Category Filtering
The custom feature added to this application is Category Filtering. While the app uses AI to automatically categorize tasks into groups like Work, Personal, or Shopping, this feature provides a functional UI dropdown that allows users to toggle between these categories. This makes the application more non-trivial by allowing users to manage and view specific subsets of their tasks rather than just seeing a single long list

Installation and Run Instructions
To run this application locally, follow these steps:
1. Clone the repository:
git clone git@github.com:DDDDOOORRI/my-todo-app.git
cd my-todo-app
2. Set up the Python Virtual Environment: 
python3 -m venv .venv
source .venv/bin/activate
pip install jaclang byllm
3. Configure your API Key: 
export ANTHROPIC_API_KEY="your-api-key-here"
4. Start the Jac Dev Server: 
jac start main.jac
Access the App: Open your browser to http://localhost:8000/.

Feature Logic and Code Location
The Category Filtering feature is implemented across the frontend and state management logic:
State Variable: Inside the app class in main.jac, a filter_cat variable was added to track the user's current selection, defaulting to "all"
Filtering Logic: I implemented a display_items list that uses a .filter() lambda function. This logic checks if the current filter_cat matches the category attribute of each Todo node; if it matches (or if "all" is selected), the item is displayed.
UI Implementation: In the return block of main.jac, a <select> dropdown menu was added with an onChange listener to update the state.
Styling: Custom CSS for the .filter-row and .category badge was added to styles.css to distinguish the categories visually.