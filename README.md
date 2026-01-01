# React Movie Explorer
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/GreatWayne-ILEARN/react-movie-explorer)

React Movie Explorer is a web application that allows users to search for movies. It fetches movie data from The Movie Database (TMDB) API and displays it in a clean, modern interface. The application also features a "Trending Movies" section, powered by Appwrite, which highlights movies based on popular user searches.

## Features

-   **Movie Search**: Search for movies by title using the TMDB API.
-   **Trending Movies**: View a list of movies that are trending based on search frequency, tracked via an Appwrite backend.
-   **Detailed Movie Cards**: View movie details including poster, title, rating, original language, and release year.
-   **Optimized API Usage**: Implements debouncing on the search input to minimize API requests while the user is typing.
-   **User Feedback**: Displays a loading spinner during data fetching and provides clear error messages.
-   **Responsive Design**: Built with Tailwind CSS for a seamless experience on desktop and mobile devices.

## Technologies Used

-   **Frontend**: React, Vite, Tailwind CSS
-   **Backend Service**: Appwrite (for search analytics)
-   **Data Source**: The Movie Database (TMDB) API
-   **Libraries**: `axios`, `react-use`

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

-   Node.js (v18 or later) and npm
-   A TMDB API Key
-   An Appwrite account and project

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/greatwayne-ilearn/react-movie-explorer.git
    cd react-movie-explorer
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project and add the following variables with your credentials:

    ```env
    VITE_TMDB_API_KEY=your_tmdb_api_key
    VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
    VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
    VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
    ```

4.  **Configure Appwrite:**
    -   Create a new project in your Appwrite console.
    -   Create a new Database.
    -   Create a Collection within that database.
    -   Add the following attributes to your collection:
        -   `searchTerm` (String, required)
        -   `count` (Integer, required)
        -   `movie_id` (Integer, required)
        -   `poster_url` (URL, required)
    -   Configure the collection's permissions to allow client-side read and write access as needed for the application's functionality.

5.  **Run the development server:**
    ```sh
    npm run dev
    ```
    The application will be available at the local address provided by Vite (e.g., `http://localhost:5173`).

## Available Scripts

In the project directory, you can run:

-   `npm run dev`: Starts the application in development mode with hot-reloading.
-   `npm run build`: Bundles the application for production.
-   `npm run lint`: Lints the source code using ESLint.
-   `npm run preview`: Serves the production build locally to preview it.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.