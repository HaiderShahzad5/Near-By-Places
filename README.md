#Places to Eat & Drink on Campus

#Purpose of the Application
The *"Places to Eat & Drink on Campus"* app provides users with an interactive way to
explore dining options on campus. With features such as a map, detailed venue
information, and the ability to sort venues by proximity, this app ensures that users can
easily discover places to eat and drink near their current location.

#Target Audience
● Students: T o find nearby cafes, food courts, or dining areas on campus.
● Faculty and Staff: T o quickly locate venues for coffee breaks or meals.
● Visitors: T o explore campus dining options during events or campus tours.

#Key Features
1. Interactive Map:
a. Displays dining venues on a map with custom annotations.
b. Shows the user's current location for easy navigation.
c. Allows users to tap on venue pins to access detailed information.
2. Proximity-Based Venue Sorting:
a. Automatically sorts venues by distance from the user's current location.
b. Helps users quickly find the nearest dining options.
3. Favorites (Like Feature):
a. Users can "like" venues by tapping a heart icon.
b. Favorites are saved in persistent storage using Core Data, ensuring
preferences remain intact across sessions.
4. Nearby Places View:
a. Toggle a list view of all venues with the ability to browse their names and
details.
b. The view dynamically updates when venues are sorted by proximity.
5. Detailed Venue Information:
a. Clicking on a venue (via the map or list) navigates to a detail screen
providing additional information about the venue.
6. Offline Access:
a. The app fetches venue data from a remote JSON API and stores it locally
using Core Data for offline access.
7. Core Data Integration:
a. Ensures venue data is persistent and can be updated without losing user
preferences.

#Core Functionalities
1. Map Features
a. Center map on user location using CLLocationManager .
b. Display all venues with annotations derived from latitude and longitude.
2. Venue Sorting
a. Sort venues dynamically based on the user's proximity using CLLocation.
3. Data Management
a. Fetch venue data from a remote JSON API.
b. Save venue details to Core Data.
c. Fetch existing venues and user preferences from Core Data if offline.
4. T able View
a. Displays a scrollable list of venues with an interactive heart button for
liking venues.
b. T apping a venue navigates to its detailed view.
5. Venue Details Screen
a. Presents all details for a selected venue in a separate view.
b. Includes name, location, and favorite status.

#Technical Architecture
● Language & Frameworks:
○ Swift
○ UIKit
○ MapKit for map-related functionality
○ CoreData for local data persistence
○ URLSession for networking and fetching remote data
● Data Flow:
○ Remote JSON API → Fetch data via
`URLSession
`
.
○ Save API data to Core Data for persistence.
○ Sync UI elements with Core Data entries.
● Error Handling:
○ Gracefully handles errors such as network failures by falling back on Core
Data.
● Performance:
○ Optimized data fetching and sorting to minimize computation overhead.
○ Uses efficient CLLocation methods for geolocation.

#Usage Guide
1. Map Navigation:
a. Open the app to view a map centered on the campus.
b. Venues are displayed as pins on the map. T apping a pin shows the venue’s
name.
2. Finding Nearby Places:
a. Tap the *"Nearby Places"* button to see a sorted list of venues based on
distance.
b. T ap on a venue to navigate to its details.
3. Marking Favorites:
a. Use the heart icon in the list view to mark venues as favorites.
b. Favorites are saved persistently, so they remain even after closing the
app.
4. Exploring Venue Details:
a. T ap on a map pin or list item to navigate to the venue’s detailed view.
5. Offline Access:
a. If offline, previously fetched data is loaded from Core Data for seamless
access.
#Future Enhancements
1. 2. 3. 4. User Reviews: Allow users to rate and review venues.
Push Notifications: Notify users of special deals or promotions.
Custom Categories: Filter venues by type (e.g.,
"Cafes,
" "Fast Food").
Enhanced Offline Mode: Add the ability to download map tiles for offline
navigation.
