# ZVote-FrontEnd

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Getting Started](#getting-started)
5. [Prerequisites](#prerequisites)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Integration with ZVote-SpringBoot](#integration-with-zvote-springboot)

---

## Project Overview
**ZVote-FrontEnd** is the JavaFX-based graphical user interface for the ZVote electronic voting system, designed to work seamlessly with the ZVote-SpringBoot backend. This application allows users to interact with voting polls, cast votes, and view results through a modern, intuitive desktop UI, leveraging RESTful communication with the backend.

---

## Features
- User login and authentication.
- Display available polls and poll details.
- Cast votes securely via the Spring Boot backend.
- Real-time results visualization.
- Full CRUD operations on polls.
- Responsive JavaFX user interface.
- Error handling and feedback dialogs.
- Easy configuration for backend URL.

---

## Architecture

ZVote-FrontEnd uses an MVC structure:

- **Model**: Java classes representing polls, votes, users, and results.
- **View**: JavaFX FXML files and UI components for all screens.
- **Controller**: Handles user actions, API requests, and updates views.

**Backend Integration**:  
All data operations (polls, votes, results) are performed by sending HTTP requests to the ZVote-SpringBoot backend via its REST API.

---

## Getting Started

Follow these steps to set up and run ZVote-FrontEnd locally.

### Prerequisites
- **Java JDK**: Version 11 or newer.
- **JavaFX SDK**: Compatible with your Java version.
- **Git**: To clone the repository.
- **ZVote-SpringBoot Backend**: Running and accessible.
- (Optional) **IDE**: IntelliJ IDEA, Eclipse, or NetBeans for development.

---

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/MateoBitar/ZVote-FrontEnd.git
    cd ZVote-FrontEnd
    ```

2. **Import the project into your IDE**:
    - Open your IDE and choose “Import Project.”
    - Select the cloned folder.
    - Set up the JavaFX SDK as a library/module if needed.

3. **Configure JavaFX SDK**:
    - Download JavaFX SDK: [https://gluonhq.com/products/javafx/](https://gluonhq.com/products/javafx/)
    - Add the JavaFX library to your project/module settings.

4. **Configure Backend URL**:
    - Locate the configuration file or constant in the codebase for the backend API URL (e.g., `http://localhost:8080/api`).
    - Update it to match your ZVote-SpringBoot instance if necessary.

5. **Build and run the project**:
    - Use your IDE’s build/run function, or from the command line:
      ```bash
      javac --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -d out src/**/*.java
      java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -cp out Main
      ```

---

## Usage

- **Login/Register**:
  - Authenticate with the backend.

- **Polls**:
  - Browse available polls and view details.
  - Create new polls.
  - Edit or delete polls.

- **Voting**:
  - Select a poll and cast your vote.
  - Receive confirmation on successful voting.

- **Results**:
  - View poll results dynamically updated from backend.

- **Error Handling**:
  - Errors and feedback are shown via JavaFX dialogs.

---

## Integration with ZVote-SpringBoot

- **REST API Communication**:
  - The frontend communicates with the backend via HTTP requests (using libraries like HttpURLConnection, HttpClient, or third-party libraries).
  - Ensure ZVote-SpringBoot is running and accessible at the configured URL.

- **Typical API Endpoints Used**:
  - `GET /api/polls` - List polls
  - `GET /api/polls/{id}` - Poll details
  - `POST /api/polls/{id}/vote` - Cast a vote
  - `GET /api/polls/{id}/results` - Fetch results
  - (Authentication endpoints as required)

- **Customizing Backend URL**:
  - Update the configuration in the code to point to your backend instance.

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request. For major changes, open an issue first to discuss your proposals.

---

## License

This project is licensed under the MIT License.

---

For additional questions or issues, please refer to the documentation or contact the repository maintainer.
