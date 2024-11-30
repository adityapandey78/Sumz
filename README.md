# Sumz: Article Summarizer Powered by AI 🚀

Sumz is a React-based web application designed to summarize lengthy articles into concise, readable insights using cutting-edge AI technologies. This project leverages **React**, **Redux Toolkit**, and **React Hooks** for efficient state management and user interaction while seamlessly integrating with an external API for summarization.

---

## Features 🌟

- 📰 Summarizes lengthy articles into concise content.
- ⚡ Real-time updates with efficient state management using **React Redux Toolkit**.
- 🔍 Input validation to ensure URLs are correctly processed.
- 🌈 A responsive and intuitive user interface built with modern React components.

---

## Technologies Used 💻

### Frontend

1. **React**  
   - **Functional Components**: Built the UI using functional components for better modularity and reuse.  
   - **React Hooks**: Simplified component logic and introduced state and lifecycle management within functional components.  
     - `useState`: To manage local states, such as input and summarized data.  
     - `useEffect`: To handle side effects like API calls when the URL changes.

2. **Redux Toolkit**  
   - Used for managing the global state, especially handling API data and application-wide states.
   - **Slices**: Modularized state logic for cleaner and more maintainable code.
   - **createAsyncThunk**: For making asynchronous API requests and handling their states (loading, success, error).

3. **React Redux**  
   - Integrated Redux Toolkit into React components seamlessly to access and manipulate the global state.

### Backend (API Integration)

- **RapidAPI**  
  The summarization feature is powered by RapidAPI's Article Summarizer API, which uses AI to generate summaries of given URLs.  
  - **API Key**: Configured securely using environment variables for safe access.  
  - **Asynchronous Fetch**: Leveraged `fetch` or Axios within a `createAsyncThunk` function to fetch summaries from the API.  
  - **Error Handling**: Implemented robust error handling to ensure smooth user experience in case of API failures.  
- **Local Storage:** Use of Local Storage to display the recent searches.  
---

## How It Works 🛠️

1. **User Input**:  
   - The user enters an article URL into the input field.

2. **API Call**:  
   - On submitting the URL, the app sends a request to the **RapidAPI Article Summarizer** endpoint.

3. **Data Management with Redux**:  
   - The app uses Redux Toolkit to manage the summarization data and update the UI with the response.  
   - API state (loading, success, error) is managed using `createAsyncThunk` and reducers.

4. **Dynamic UI Updates**:  
   - As soon as the API response is received, the UI updates dynamically to display the summarized content.

---

## Installation Guide 🛠️

To get started with Sumz, follow these steps:

### 1. Clone the Repository
Clone the repository to your local machine using:
```bash
git clone https://github.com/adityapandey78/Sumz.git
cd Sumz
```

### 2.Install Dependencies
```bash
npm install
```
### 3.Set up environment variables:
- Create a `.env` file in the root directory.  
- Add your RapidAPI key
```env
REACT_APP_RAPIDAPI_KEY=your_api_key_here
```
### 4.Run the application:  
```bash
npm run dev
```
## Directory Structure 📁  
```bash
Sumz/
├── public/
├── src/
│   ├── components/       # Reusable UI components
│   ├── features/         # Redux slices and API logic
│   ├── hooks/            # Custom hooks for modularity
│   ├── App.js            # Main application entry
│   ├── index.js          # Root file for ReactDOM rendering
│   ├── store.js          # Redux store configuration
├── .env                  # Environment variables (API keys)
├── package.json          # Dependencies and scripts
```  
## Future Enhancements🚀 

-🌐 Multi-language support for summarization.  
-📊 Analytics to provide insights into article engagement.  
-🌙 Dark mode for better user experience.