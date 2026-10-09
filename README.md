# Recipe Finder

A premium recipe discovery website built with React, Vite, TypeScript, and Tailwind CSS.

## Features

- Search recipes by name or ingredient
- Browse curated recipe categories and cuisine filters
- View detailed recipe instructions and ingredients
- Save favorites with localStorage persistence
- Responsive layout with accessible interactions
- Typed TheMealDB API integration for recipe search, filters, lookup, and random discovery
- Loading, empty, retry, and API error states

## API choice

This project uses TheMealDB because it is public, simple to integrate, and does not require private client-side credentials for basic usage.

- API base URL: https://www.themealdb.com/api/json/v1
- API key: `1` for the public test key; configure your own key where required
- Documentation: https://www.themealdb.com/api.php
- Availability: Public access for non-commercial use with rate limits and occasional downtime

## Local setup

1. Install dependencies:
   npm install
2. Copy the example environment file:
   copy .env.example .env
3. Start the development server:
   npm run dev

## Environment variables

- `VITE_RECIPE_API_BASE_URL`: Optional API root override. Include `/v1`, but not the API key.
- `VITE_RECIPE_API_KEY`: Optional key appended to the API root (defaults to `1`). An existing full base URL ending in `/v1/{key}` is also accepted.

## Notes

- TheMealDB does not provide reliable cooking-time metadata, serving sizes, or strict dietary filters for every recipe.
- The UI only displays recipe metadata supplied by TheMealDB; calorie, rating, cooking-time, serving-size, and nutrition claims are not inferred.
- Favorites persist in the browser with localStorage and are restored after refresh.
