# Simple Python Web Application

A simple Flask web application that displays "Steven is Learning Devops" in the browser.

## Running the Application Locally

### Prerequisites
- Python 3.6 or higher
- pip (Python package manager)

### Steps

1. Clone or download this repository
2. Navigate to the project directory:
   ```
   cd python_web_app
   ```
3. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```
5. Run the application:
   ```
   python app.py
   ```
6. Open your web browser and navigate to:
   ```
   http://localhost:5000
   ```

## Running as a Docker Container

### Prerequisites
- Docker installed on your system

### Steps

1. Navigate to the project directory:
   ```
   cd python_web_app
   ```
2. Build the Docker image:
   ```
   docker build -t devops-learning-app .
   ```
3. Run the Docker container:
   ```
   docker run -p 5000:5000 devops-learning-app
   ```
4. Open your web browser and navigate to:
   ```
   http://localhost:5000
   ```

## Stopping the Application

- If running locally: Press `Ctrl+C` in the terminal
- If running as a Docker container: 
  ```
  docker ps  # Find the container ID
  docker stop <container_id>
  ```
