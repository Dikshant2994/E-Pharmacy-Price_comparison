Project Explanation – E-Pharmacy Price Comparison
_________________________________________________
Introduction
•	The "E-Pharmacy Price Comparison" project uses Python with the Streamlit library for interactive dashboard creation and SerpAPI for real-time data retrieval.
•	This system allows users to search for any medicine and instantly compare prices across multiple online pharmacies.
•	The goal is to address price transparency issues in the online medicine market and help consumers identify the most cost-effective option.
•	The dashboard also provides visual comparisons through bar and pie charts, making the data easy to interpret.
________________________________________
Data Collection
•	Data is collected dynamically from Google Shopping search results using the SerpAPI.
•	The system retrieves:
o	Medicine title
o	Company/Source (online pharmacy name)
o	Price
o	Thumbnail image
o	Purchase link
•	User inputs:
o	Medicine name
o	Number of options to compare
________________________________________
Libraries Used
•	pandas for data manipulation and structuring.
•	matplotlib.pyplot for pie chart visualizations.
•	streamlit for building the interactive user interface.
•	serpapi for fetching real-time medicine price data from Google Shopping.
________________________________________
Data Loading
•	Unlike static datasets, this project fetches live data from the web through an API call.
•	User input parameters (medicine name and number of options) are passed to SerpAPI.
•	Results are returned in JSON format, from which relevant fields (source, title, price, product link, image) are extracted.
________________________________________
Dashboard Layout
Streamlit Components
•	Sidebar:
o	Medicine name input field.
o	Number of comparison options input.
o	“Price Compare” button.
•	Main Page:
o	Project logo and title.
o	List of available options with company name, product title, price, image, and buy link.
o	Highlighted “Best Option” section displaying the lowest price found.
o	Bar chart and pie chart for price comparisons.
________________________________________
Divisions and Structure
•	Columns in Streamlit:
o	Used to display details in a clean, side-by-side layout (company, title, price, link).
•	Best Option Display:
o	Dynamically updates to show the cheapest available product based on retrieved prices.
________________________________________
Styling and External Dependencies
•	Streamlit’s built-in layout tools are used for structuring the interface.
•	Matplotlib is used for pie chart plotting.
•	Streamlit’s st.bar_chart method is used for instant bar chart creation.
•	The project could be extended with Bootstrap CSS or custom HTML/CSS for enhanced styling.
________________________________________
Running the Application
•	The application is launched locally using:
•	streamlit run app.py
•	Once launched, it opens in the default web browser.
•	Users can enter a medicine name and view comparison results instantly.
________________________________________
Challenges Faced and Solutions
•	Challenge: Handling inconsistent price formats from SerpAPI responses.
Solution: Implemented string cleaning (removing currency symbols, replacing commas, converting to floats).
•	Challenge: Ensuring correct display when fewer results are returned than requested.
Solution: Added logic to process only available options without errors.
•	Challenge: Managing API call limits.
Solution: Optimized queries to return only essential fields.
________________________________________
Conclusion
This project enhanced my skills in API integration, real-time data handling, and interactive dashboard creation with Streamlit.
It demonstrates how data science techniques can be applied to consumer-oriented price comparison systems, offering a practical solution to help people make informed purchasing decisions.
