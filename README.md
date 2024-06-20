# Skill Builder Workshop Finder API

The Skill Builder Workshop Finder API provides access to a wide range of workshops based on users' interests and multiple other parameters. Our API is designed to offer information on various workshops, including art, technology, and more.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [Setup and Configuration](#setup-and-configuration)
- [Operations](#Operations)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Skill Builder Workshop Finder API is developed to provide users with a robust system for finding and filtering workshops. It integrates with various AWS services to ensure scalability, reliability, and performance, supporting high volumes of concurrent users.

## Features

- **Workshop Retrieval**: Fetch details about various workshops.
- **Filtering Options**: Filter workshops based on keywords, dates, and other parameters.
- **Caching**: Utilize distributed caching to improve response times and reduce database load.
- **Monitoring**: Real-time monitoring with AWS CloudWatch.

## Technologies

The project is built with the following technologies:

- **Node.js**: A JavaScript runtime for building the backend.
- **Express.js**: A web application framework for Node.js.
- **MongoDB Atlas**: For scalable and flexible data storage.
- **AWS Lambda**: For serverless computing.
- **AWS API Gateway**: For managing and securing API calls.
- **AWS CloudWatch**: For monitoring and error handling.

## Installation

To run this project locally, follow these steps:

### Prerequisites

- Node.js
- npm or yarn
- MongoDB Atlas account
- AWS account

### Setup

1. Install the dependencies:
    ```bash
    npm install

2. Set up the environment variables in the .env file.

3. Start the backend server:
    ```bash
    npm start

## Usage
Once the server is running, you can access the API endpoints to retrieve and filter workshop information.

## Environment Variables
Ensure you have the necessary environment variables set up. You can find a sample configuration in the .env file. Here are the key variables:

1. `PORT`: Port for the server.
2. `MONGODB_URI`: MongoDB connection string.
3. `AWS_ACCESS_KEY_ID`: AWS access key for accessing AWS services.
4. `AWS_SECRET_ACCESS_KEY`: AWS secret key for accessing AWS services.

## API Endpoints
### Workshop Endpoints
1. GET /workshops: Retrieve a list of workshops with the ability to filter results based on specific criteria.
2. GET /workshops/: Retrieve details of a specific workshop by its ID.

### Example Requests

Get All Workshops
``` bash
GET /workshops
```

Get Workshop by ID
``` bash
GET /workshops/:id
```

Filter Workshops by Keyword
``` bash
GET /workshops?keywords=art
```

Filter Workshops by Date Range
``` bash
GET /workshops?startDate=2024-06-01&endDate=2024-06-30
```

### Query Parameters for GET /workshops
`location` (optional): Filter workshops by location.
`startDate` and `endDate` (optional): Filter workshops within a specific date range.
`keywords` (optional): Filter workshops based on specific keywords.

### Path Parameters for GET /workshops/
`id` (required): The unique identifier of the workshop to retrieve.

### Response Format
The response will be in JSON format. Here is an example of a successful response for the GET `/workshops` endpoint:

```bash
{
  "id": "65e4534khj4b408a2936jcd48925",
  "title": "Watercolor Painting for Beginners",
  "category": "Art",
  "description": "Dive into the basics of watercolor painting with expert guidance.",
  "location": "Central Park, New York",
  "date": "2024-04-15",
  "price": 50,
  "participantLimit": 15,
  "registrationCount": 5,
  "instructorBio": "Alex Johnson, an award-winning artist known for vibrant landscapes.",
  "tags": ["watercolor", "painting", "art"]
}
```
## setup-and-configuration

### Node.js
1. Initialize the Node.js project:
    ```bash
    npm init

2. Install necessary packages:
    ```bash
    npm install


### AWS Services Configuration
1. AWS Lambda: Deploy serverless functions for backend logic.
2. AWS API Gateway: Configure API Gateway to manage and secure API calls.
3. AWS CloudWatch: Set up monitoring and logging for the API.

### Database Configuration
1. MongoDB Atlas: Set up the database cluster and configure connection strings.

## Contributing
We welcome contributions from the community. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (git checkout -b feature-branch).
3. Make your changes.
4. Commit your changes (git commit -m 'Add some feature').
5. Push to the branch (git push origin feature-branch).
6. Open a Pull Request.

## License
This project is licensed under the MIT License.

