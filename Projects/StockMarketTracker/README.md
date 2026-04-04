# Stock Market Tracker

A React stock tracking app that lets users search companies, inspect stock details, view recent price history, manage a watchlist, and build a simple portfolio dashboard.

## Features

- Search stocks by symbol or company name
- View company overview and latest daily price data
- See a recent 5-day price table
- Visualize closing prices with a 30-day chart
- Add stocks to a watchlist
- Add stocks to a portfolio and update share quantity
- Toggle between light and dark themes

## Tech Stack

- React 19
- Vite 7
- Redux Toolkit
- React Router
- Recharts
- Tailwind CSS
- Alpha Vantage API

## Getting Started

1. Install dependencies:

```bash
npm install
```

2. Create a `.env` file in the project root:

```env
VITE_ALPHA_VANTAGE_API_KEY=your_api_key_here
```

3. Start the development server:

```bash
npm run dev
```

4. Build for production:

```bash
npm run build
```

5. Preview the production build:

```bash
npm run preview
```

## How It Works

- Stock search uses Alpha Vantage symbol search.
- The details page fetches both company overview data and daily time series data.
- Portfolio and watchlist items are managed with Redux Toolkit.
- The chart displays recent closing prices with Recharts.

## Environment Variable

- `VITE_ALPHA_VANTAGE_API_KEY` is required for all API requests

## API Notes

- This project uses `https://www.alphavantage.co/query`
- Alpha Vantage has request limits on the free tier
- If the limit is reached, the app shows a message asking the user to wait and try again

## Current Behavior

- Portfolio and watchlist state are stored in Redux memory only
- Theme preference is saved in `localStorage`
- Refreshing the page resets portfolio and watchlist data

## Project Structure

```text
src/
  app/
  features/
    portfolio/
    stocks/
    watchlist/
  services/
  App.jsx
  index.css
  main.jsx
```

## Scripts

- `npm run dev` - start the Vite dev server
- `npm run build` - create a production build
- `npm run preview` - preview the production build
- `npm run lint` - run ESLint
