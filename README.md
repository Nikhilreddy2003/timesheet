# Daily Timesheet Application

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

A clean, modern, and serverless **Daily Timesheet Web Application** designed for consultancies and freelancers to easily track and submit their daily work hours. 

## 🚀 Live Demo

[View the Live Application on Vercel](https://timesheet-nikhilreddy2003.vercel.app/)

*(Note: The link above assumes the default Vercel deployment name. If the Vercel link is different, please update this link).*

## ✨ Features

*   **Modern UI/UX**: Built with a sleek, responsive design featuring glassmorphism, smooth animations, and beautiful typography (Inter & Outfit fonts).
*   **Serverless Backend**: Utilizes Google Forms as an invisible backend to collect and store timesheet submissions directly into a Google Sheet without the need for a traditional database or server.
*   **Dynamic Calculations**: Automatically calculates total hours worked and categorizes billable vs. non-billable hours in real-time.
*   **CSV Export**: Instantly export the daily timesheet to a locally downloaded CSV file for offline record keeping.
*   **Categorization**: Track tasks by specific projects and categorize time as Billable, Non-Billable, or Internal.

## 🛠️ Built With

*   **HTML5 & CSS3**: For the structural foundation and styling, keeping the app lightweight without bulky frameworks.
*   **Vanilla JavaScript (ES6)**: To handle DOM manipulation, dynamic time calculation, CSV generation, and seamless Google Forms submission.
*   **Phosphor Icons**: For clean and consistent iconography.

## 📥 How the Google Forms Backend Works

To keep the application entirely frontend and free to host, it uses a clever trick to submit data directly to a Google Form:
1.  The user fills out the timesheet.
2.  Upon clicking "Submit", JavaScript gathers the data and formats it into a structured text block.
3.  A hidden `<iframe>` and HTML `<form>` are dynamically created in the DOM.
4.  The form's action is pointed to the Google Form's specific `formResponse` URL.
5.  The payload is submitted to the exact `entry.[id]` matching the Google Form question.
6.  The data bypasses the Google Forms UI and lands directly in the owner's Google Sheet!

## ⚙️ Setup Instructions (For your own clone)

If you want to clone this repository and set up your own Google Forms backend:
1.  Create a blank Google Form with a single "Paragraph" text question.
2.  Get the Form's `formResponse` URL and the specific `entry.[id]` for that question (you can find this by inspecting the actual Google Form HTML).
3.  Open `index.html` and locate the `submitSheet()` function.
4.  Replace the `googleFormActionURL` and `formEntryID` variables with your specific URLs.
5.  Deploy the HTML file to any static host (like Vercel, Netlify, or GitHub Pages)!

## 📄 License

This project is free to use and modify for personal or commercial tracking purposes.
