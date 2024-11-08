Coding Quiz

This project is a full-stack coding quiz application where users can answer questions about programming languages like Python. The application features a responsive front end built with Vite and a back end powered by Node.js, Express, and MongoDB. It includes a GitHub Actions CI/CD pipeline that automates testing and deployment.

Table of Contents

	•	About the Project
	•	Features
	•	Tech Stack
	•	Setup and Installation
	•	Usage
	•	Database Seeding
	•	Testing and CI/CD
	•	Contributing
	•	License

About the Project

This application allows users to take quizzes on programming topics, starting with Python questions. The application is designed to be a simple and interactive learning tool for anyone looking to test or expand their knowledge of coding concepts.

Features

	•	Multiple-choice quiz questions stored in a MongoDB database.
	•	Front end built with Vite for fast and efficient loading.
	•	Backend server with Express and MongoDB.
	•	Continuous Integration (CI) with GitHub Actions to run Cypress tests on pull requests.
	•	Continuous Deployment (CD) to Render when changes are merged into the main branch.

Tech Stack

	•	Frontend: Vite, HTML, CSS
	•	Backend: Node.js, Express.js
	•	Database: MongoDB
	•	CI/CD: GitHub Actions
	•	Deployment: Render

Setup and Installation

Prerequisites

	•	Node.js and npm installed.
	•	MongoDB installed and running locally, or a cloud instance.
	•	Render account for deployment.

Installation

	1.	Clone the repository:
    git clone https://github.com/your-username/coding-quiz.git
    cd coding-quiz

    2.	Install server and client dependencies:
    npm install
    cd server && npm install
    cd ../client && npm install

    3.	Configure Environment Variables:
    •	Create a .env file in the server folder.
	•	Set up the following environment variables:
    MONGODB_URI=mongodb://localhost:27017/your-database

Usage

	1.	Build and Start the Application: npm start
    •	The server will start at http://localhost:3001.
	•	You can access the client build files at http://localhost:3000.

    2.	Run in Development Mode: npm run dev

    3.	Accessing the Application:
	•	Navigate to http://localhost:3001 to view the application.

Database Seeding

To seed the database with initial Python quiz questions:
	1.	Ensure MongoDB is running.
	2.	Run the seeding script: npm run seed
    This command will delete existing documents in the Question collection and insert new questions from the pythonQuestions.json file.

Testing and CI/CD

This project uses GitHub Actions for automated testing and deployment.

Continuous Integration (CI)

	•	Cypress Tests: On each pull request to the develop branch, GitHub Actions runs Cypress tests to ensure new changes do not break the app.

Continuous Deployment (CD)

	•	Render Deployment: When changes are merged from develop to main, GitHub Actions triggers a deployment to Render, where the app is hosted.

GitHub Actions Workflow Setup

The .github/workflows folder includes:
	•	test.yml: Runs Cypress tests on pull requests to develop.
	•	deploy.yml: Deploys the app to Render when code is merged into main.

Contributing

Contributions are welcome! Please fork the repository and create a pull request from your feature branch to develop.
	1.	Fork the project.
	2.	Create your feature branch (git checkout -b feature/YourFeature).
	3.	Commit your changes (git commit -m 'Add your message here').
	4.	Push to the branch (git push origin feature/YourFeature).
	5.	Open a pull request.

License

This project is licensed under the MIT License.

Contact

For any questions or feedback, please reach out at [kol3wang@gmail.com].