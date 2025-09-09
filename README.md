# Mobile App with Database

A React Native mobile app built with Expo that includes user authentication and database functionality using Supabase.

## Features

- 📱 Cross-platform mobile app (iOS, Android, Web)
- 🔐 User authentication (sign up, sign in, sign out)
- 👤 User profiles with customizable information
- 📊 Database integration with Supabase
- 🔒 Row Level Security (RLS) for data protection
- 📱 Device-specific user data storage

## Setup Instructions

### 1. Supabase Setup

1. Click the "Connect to Supabase" button in the top right of Bolt
2. Create a new Supabase project or connect to an existing one
3. Your Supabase credentials will be automatically added to the `.env` file

### 2. Database Migration

The app includes a database migration that creates the `user_profiles` table with proper security policies. This will be automatically applied when you connect to Supabase.

### 3. Running the App

```bash
# Start the development server
npm start

# Run on specific platforms
npm run android  # Android emulator/device
npm run ios      # iOS simulator/device
npm run web      # Web browser

# For testing on physical devices over network
npm run start:tunnel
```

## App Structure

- **Auth Component**: Handles user registration and login
- **UserProfile Component**: Manages user profile data and device information
- **Supabase Integration**: Database operations with authentication
- **Row Level Security**: Ensures users can only access their own data

## Database Schema

### user_profiles table
- `id`: User ID (references auth.users)
- `email`: User's email address
- `full_name`: User's display name
- `device_info`: Device-specific information
- `created_at`: Account creation timestamp
- `updated_at`: Last profile update timestamp

## Security Features

- Email/password authentication
- Row Level Security policies
- User data isolation
- Secure session management
- Automatic token refresh

## Development

The app uses:
- **Expo**: React Native development platform
- **Supabase**: Backend as a Service
- **TypeScript**: Type safety
- **React Native Elements**: UI components

## Deployment

This app can be deployed to:
- iOS App Store (via Expo Application Services)
- Google Play Store (via Expo Application Services)
- Web (as a Progressive Web App)

For production deployment, you'll need to:
1. Configure app signing
2. Set up proper environment variables
3. Build and submit through Expo EAS