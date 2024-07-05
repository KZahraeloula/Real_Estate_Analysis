# real-estate-project3

Problem to Solve:

We aim to investigate the relationship between real estate values and household income in the tristate area (New York, New Jersey, and Connecticut). Specifically, we want to determine whether higher household incomes in certain ZIP codes correlate with higher real estate prices in those same areas. By analyzing and comparing these datasets, we seek to uncover patterns and insights that can inform our understanding of real estate market dynamics and economic conditions across different regions within the tristate area.

Data Cleanup and Analysis:

After selecting our datasets from Kaggle (USA Real Estate Dataset and US Household Income by ZIP Code), we explored and cleaned the data to include only the relevant information for the story we wanted to tell and the information we wanted to explore. We narrowed the USA real estate dataset to include only the tristate area and removed the column titled prev_sold_date. For the US Household Income data, we honed in exclusively on Household income, excluding categories such as Families, Married-Couple Families, and Nonfamily Households. 

Project Architecture:

Backend (Data & Logic):

SQL Database: Choose a robust database like PostgreSQL or MySQL to store your real estate data (median income, average prices, ZIP codes, etc.). Design a schema with well-normalized tables.
Flask (Python Web Framework):
Create RESTful API endpoints to:
Fetch data from the database based on user queries (e.g., filter by ZIP code, year range).
Aggregate data for calculations (e.g., average prices, income distribution).
Return data in JSON format for easy consumption by the frontend.
Frontend (User Interface):

HTML: Structure the web page layout, including:
Map container for Leaflet.
Chart containers for D3.js visualizations.
User input elements (dropdowns, sliders, etc.).
CSS: Style the elements to create a visually appealing and user-friendly interface.
JavaScript (Leaflet & D3.js):
Leaflet:
Initialize an interactive map.
Load geoJSON data for the tri-state area.
Create choropleth maps (color-coded regions) based on income or housing prices.
Add markers, popups, and other interactive features.
D3.js:
Create bar charts, scatterplots, line graphs, or other visualizations.
Make them interactive (e.g., tooltips on hover, zoom/pan).
Use transitions and animations for smooth updates.
Development Steps:

Database Setup:

Install your chosen SQL database.
Create the database schema and populate it with your real estate data.
Flask API Development:

Install Flask and necessary libraries (e.g., SQLAlchemy for database interaction).
Define routes and functions to handle API requests from the frontend.
Thoroughly test your endpoints.
Frontend Development:

Set up an HTML, CSS, and JavaScript project structure.
Include Leaflet and D3.js libraries.
Design the user interface layout.
Implement map and chart components.
Write JavaScript code to:
Make API calls to the Flask backend.
Process the returned data.
Render visualizations dynamically based on the data and user interactions.
Key Features (Examples):

Interactive Map: Users can click on a ZIP code to see details like median income, average house prices, and historical trends.
Filterable Charts: Users can select years or ZIP code ranges to update charts accordingly.
Trend Lines: Display trend lines on charts to show changes in income or prices over time.
Data Comparison: Allow users to compare income and prices across different ZIP codes or time periods.
Responsiveness: Ensure the web app works well on different screen sizes (desktop, tablet, mobile).
Additional Tips:

Data Cleaning: Invest time in thorough data cleaning to ensure accurate and reliable visualizations.
Error Handling: Implement robust error handling to gracefully manage unexpected errors.
Caching: Consider caching frequently accessed data on the server-side to improve performance.
Documentation: Document your code and API endpoints for future reference.
