# MovieFlix

MovieFlix is a React Native app built with Expo and `expo-router`. It provides a modern movie discovery experience using data from The Movie Database (TMDB). The app includes a home screen with latest movies, a search entry point, and a tab-based structure for future expansion.

## Key features

- Expo + React Native app using `expo-router` for file-based navigation
- Home screen with a movie list fetched from TMDB
- Custom movie cards showing title, rating, release year, and poster images
- Tab navigation skeleton with placeholders for `Search`, `Saved`, and `Profile`
- NativeWind styling with Tailwind-friendly utility classes
- Asset-driven UI using centralized icon and image constants

## Project structure

- `app/` - main app routes and screens
  - `app/(tabs)/index.tsx` - home screen displaying the movie feed
  - `app/(tabs)/search.tsx` - search screen placeholder
  - `app/(tabs)/saved.tsx` - saved movies placeholder
  - `app/(tabs)/profile.tsx` - profile placeholder
  - `app/movies/[id].tsx` - movie detail route stub
  - `app/_layout.tsx` - root stack layout
- `app/components/` - reusable UI components
  - `MovieCard.tsx` - movie card component used in the list
  - `SearchBar.tsx` - search input component
- `app/services/` - API helper and data fetching logic
  - `api.ts` - TMDB movie fetch helper
  - `useFetch.ts` - custom hook for loading state and async fetch
- `assets/` - icon and image assets used by the app
- `constants/` - centralized image and icon references

## Setup

1. Install dependencies

```bash
npm install
```

2. Create a local environment file

Create a `.env` file at the project root with your TMDB key:

```env
EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_api_key_here
```

> The app reads `EXPO_PUBLIC_MOVIE_API_KEY` from `process.env` to access TMDB.

3. Start the development server

```bash
npx expo start
```

4. Launch on a device or emulator

- Android: `npm run android`
- iOS: `npm run ios`
- Web: `npm run web`

## Notes

- The `Search`, `Saved`, and `Profile` screens are currently placeholders.
- The `movies/[id]` screen is currently a stub and can be expanded with detailed movie content.
- The home screen shows popular movies using TMDB's discover endpoint.

## Technology stack

- `expo`
- `react`
- `react-native`
- `expo-router`
- `nativewind`
- `tailwindcss`
- `@react-navigation/bottom-tabs`

## GitHub remote

This repository can be pushed to `https://github.com/exhorte/MovieFlix.git` once the remote is configured.
