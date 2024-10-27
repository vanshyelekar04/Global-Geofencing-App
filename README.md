# Global Geofencing App

The Global Geofencing App is a robust location-based service (LBS) system designed to help users find and connect with others in nearby locations based on geofencing and machine learning. By setting up a root location (home base) and configuring custom geofence boundaries, users can discover other travelers or people within the specified radius, fostering new connections and networking opportunities.

## Features

- **User Registration & Secure Login**: Secure registration and login functionality with passwords hashed using `Werkzeug`. This ensures that user credentials are safely stored.
- **Automatic & Manual Location Detection**: Users can let the app auto-detect their current location through IP geolocation or manually input a location for more control.
- **Geofencing Radius Customization**: Users can define a geofence boundary by adjusting the radius (in kilometers) with an interactive slider, helping them customize the search area for nearby users.
- **Real-Time Map Display**: The app integrates with Google Maps, displaying real-time user locations on a map. Users can click links to view other users’ locations on Google Maps, making location-based interactions straightforward.
- **Machine Learning-Based User Clustering**: The app utilizes clustering algorithms (`hdbscan`, `Birch`, `MiniSom`) to group users based on proximity and relevance, ensuring that users only see the most relevant results based on their geofence.

## How It Works

1. **Root Location**: Upon registration, users set a "root" location (e.g., home base) to act as their reference location.
2. **Travel Detection**: When a user moves to a new location, they can update their current coordinates manually or allow automatic detection.
3. **Proximity Matching**: The app calculates the distance between users based on the Haversine formula, helping determine who is within a specific radius. 
4. **Real-Time Updates**: Once logged in and with the location set, users can adjust the geofence radius, automatically updating nearby results shown on the Google Map.
5. **Tracking Links**: Users can access other users’ tracking links to view precise locations on Google Maps, making the app ideal for networking, meetups, and more.

## Prerequisites

Ensure the following are installed before running the app:

- **Python 3.7+**
- **Google Maps API Key**: Obtain a [Google Maps API Key](https://developers.google.com/maps/documentation/javascript/get-api-key) for geolocation and map services.

## Installation

1. **Clone this repository**:

   ```bash
   git clone https://github.com/vanshyelekar04/Global-Geofencing-App.git
   cd Global-Geofencing-App
