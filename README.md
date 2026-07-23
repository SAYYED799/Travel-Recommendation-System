# Travel-Recommendation-System
Welcome to the Travel Recommendation System! This project helps you discover the best travel destinations, restaurants, and connect with fellow travelers based on your preferences.

Table of Contents
Features
Project Structure
Setup Instructions
How to Use
Image Processing (Optional)
Troubleshooting
Credits
Features
Personalized Travel Recommendations: Get destination suggestions based on your travel type, budget, season, and style.
Restaurant Finder: Discover popular restaurants at each destination.
Social Features: Add friends, join travel groups, and share experiences.
Wishlist: Save destinations you want to visit.
User Reviews: Read and write reviews for destinations.
Project Structure
DBMS/
│
├── database.sql           # SQL file to set up the database and sample data
├── server.js              # Main backend server (Node.js + Express)
├── package.json           # Project dependencies and scripts
├── image-processor.js     # Script to convert images for the app (optional)
├── public/
│   ├── index.html         # Main web page
│   ├── script.js          # Frontend logic (JavaScript)
│   ├── styles.css         # Website styling (CSS)
│   └── images/
│       └── destinations/  # Destination images (auto-generated)
├── raw-images/            # Source images (WebP/JPG) for processing
├── fix-images.sql         # (Optional) SQL for image fixes
├── update-images.sql      # (Optional) SQL for updating images
└── README.md              # This file
Setup Instructions
1. Install Prerequisites
Node.js (Download from nodejs.org)
MySQL (Download from mysql.com)
2. Clone the Repository
git clone https://github.com/RishiPuli/Travel-Recommendation-System.git
cd Travel-Recommendation-System
3. Install Node.js Dependencies
npm install
4. Set Up the Database
Open MySQL Workbench or your preferred MySQL client.

Run the SQL script to create the database and tables:

Open the file database.sql
Copy all its contents and run it in your MySQL client.
This will create a database called travelrecommendationdb and fill it with sample data.

Update Database Credentials (if needed):

Open server.js
Find the section:
const db = mysql.createConnection({
    host: 'localhost',
    user: 'root',
    password: 'rsvr@msi',
    database: 'travelrecommendationdb'
});
Change user and password to match your MySQL setup.
5. Start the Server
npm start
or for development (auto-restarts on changes):

npm run dev
The app will be available at: http://localhost:3000
How to Use
Open your browser and go to http://localhost:3000
Explore the Home Page: Click "Get Started" to enter your travel preferences.
View Recommendations: See destinations tailored to your choices.
Register/Login: Create an account to save wishlists, write reviews, and use social features.
Restaurants & Social: Check out restaurants, add friends, and join travel groups.
Image Processing (Optional)
If you want to update or add new destination images:

Place your .webp or .jpg images in the raw-images/ folder.
Name them like: bali-paradise.webp, paris-getaway.jpg, etc.

Run the image processor:

node image-processor.js
This will convert and resize images, saving them to public/images/destinations/.
