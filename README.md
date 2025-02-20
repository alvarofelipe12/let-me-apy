# Let Me APY

A simple CORS proxy built with Node.js and Express, designed for personal projects where certain APIs may block direct access due to CORS policies.

## Features
- Proxy requests to bypass CORS restrictions.
- Built with Node.js and Express.
- Easy to deploy and use for personal projects.

## How It Works
The proxy intercepts requests and forwards them to the target API, bypassing CORS restrictions. This allows you to access APIs that would otherwise block direct requests from your frontend application.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/alvarofelipe12/let-me-apy.git
   cd let-me-apy
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the server:

   ```bash
   npm start
   ```

   The server will run on `http://localhost:3000` by default.

## Usage

Make a request to the proxy with the URL you want to access as a query parameter:

```
http://localhost:3000/?url=https://example.com/api
```

Replace `https://example.com/api` with the API endpoint you want to access.

## Deployment

### Vercel Deployment

1. Add a `vercel.json` file to the root of the project with the following content:

   ```json
   {
     "rewrites": [
       { "source": "/(.*)", "destination": "/index.js" }
     ]
   }
   ```

2. Push your repository to GitHub (or any other supported platform).

3. Go to [Vercel](https://vercel.com/) and create a new project.

4. Import your repository and set up the build settings as follows:
   - Build Command: `npm install`
   - Output Directory: `.`

5. Deploy the project.

Once deployed, you can use the proxy with your Vercel deployment URL:

```
https://your-vercel-app-url.vercel.app/?url=https://example.com/api
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

