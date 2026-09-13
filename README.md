# IP Location Detector
A simple web-based IP location detector that retrieves a visitor's public IP address, country, city, and ISP using an external IP geolocation API.

 # Overview
This project demonstrates how a frontend web application can retrieve publicly available connection information and display it in a simple, user-friendly interface.

The application uses JavaScript's fetch() API to request IP and geolocation information and dynamically displays the returned data on the webpage.

# Features
🌐 Detects the visitor's public IP address
🌍 Displays the visitor's country
📍 Displays the detected city
📡 Displays the Internet Service Provider (ISP)
⚡ Retrieves information dynamically without refreshing the page
🛡️ Includes basic error handling
📱 Responsive and simple interface
🛠️ Technologies Used
HTML5 — Page structure
CSS3 — Styling and layout
JavaScript — API requests and dynamic content
IP Geolocation API — IP and location information
📂 Project Structure
ip-location-detector/
│
├── index.html
├── style.css
└── README.md

# Getting Started
1. Clone the repository
git clone https://github.com/your-username/ip-location-detector.git

2. Open the project
Navigate into the project directory:

cd ip-location-detector

3. Run the application
Open index.html in your web browser.

For the best experience, you can also run the project using a local development server such as VS Code Live Server.

# How It Works
When the webpage loads, JavaScript sends a request to the IP geolocation API:

fetch("https://ipwho.is/")

The API returns information such as:

IP address
Country
City
ISP
The returned information is then inserted into the webpage using JavaScript:

document.getElementById("result").innerHTML = `
    IP Address: ${data.ip}<br>
    Country: ${data.country}<br>
    City: ${data.city}<br>
    ISP: ${data.connection.isp}
`;

 # Important Notes
This project detects the public IP address visible to the external API. It does not reveal a device's private/local IP address such as 192.168.x.x.

IP-based geolocation is approximate and may not represent the user's exact physical location.

The accuracy of the country, city, and ISP information depends on the geolocation service and its database.

 # Privacy
This project is intended for educational purposes. Users should be informed that their public IP address is being sent to an external IP geolocation service when they use the application.

Do not use the project to collect, store, or distribute IP addresses without appropriate notice, consent, and compliance with applicable privacy laws.

 # Purpose
This project was created as a practical demonstration of:

Working with external APIs
Using JavaScript fetch()
Processing JSON responses
Dynamically updating HTML
Handling API errors
Separating HTML, CSS, and JavaScript responsibilities
📄 License
This project is available for educational and personal use. You may modify and adapt the code for your own projects.
