# AI Virtual Trial Room

An AI-powered virtual trial room that allows users to see how clothes fit on them before buying. Upload your photo and a garment image to get a realistic virtual try-on, complete with a fit assessment and style recommendations.

## Features

- Browse products by category (T-Shirts, Shirts, Pants, Sarees).
- Search for specific products.
- View detailed product information.
- Add/remove items from a wishlist.
- **Virtual Try-On:** Upload your photo to see how a garment looks on you, powered by the Gemini API.
- Get an AI-generated fit assessment and style recommendations.
- Light/Dark mode toggle.
- Responsive design for all screen sizes.

## How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd <repository-folder>
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up Environment Variables:**
    - Create a `.env` file in the root directory.
    - Add your API Key: `API_KEY=your_gemini_api_key_here`

4.  **Start the development server:**
    ```bash
    npm run dev
    ```
    The application will be available at `http://localhost:5173`.

## Deployment

### Deploy to Vercel (Recommended)

1.  Push your code to a GitHub repository.
2.  Import the project into Vercel.
3.  **Crucial Step:** In the Vercel deployment settings, go to **Environment Variables**.
4.  Add a new variable:
    - **Name:** `API_KEY`
    - **Value:** Your Google Gemini API Key.
5.  Click **Deploy**.

### Deploy to GitHub Pages

1.  **Update Configuration:**
    - **`package.json`**: Update the `homepage` field.
      ```json
      "homepage": "https://<Your-Username>.github.io/<repo-name>",
      ```
    - **`vite.config.js`**: You may need to add `base: '/<repo-name>/'` inside `defineConfig` if not using a custom domain.

2.  **Deploy:**
    ```bash
    npm run deploy
    ```
    *Note: For GitHub Pages, you must ensure the API Key is handled securely or injected during the build action.*
