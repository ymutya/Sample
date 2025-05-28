Setting Up a FastAPI Application with Neo4j Backend for a Knowledge Graph

FastAPI Overview
FastAPI is a modern, high-performance web framework for building APIs with Python. It is designed for speed and ease of use, leveraging Python type hints to enable automatic API documentation and validation. Built on Starlette and Pydantic, it provides an efficient and developer-friendly API development experience.

Uvicorn Overview
Uvicorn is an ASGI web server implementation for Python, designed for asynchronous applications. It is lightweight and supports WebSockets and HTTP/2, making it a preferred choice for running FastAPI applications efficiently.

Prerequisites
Neo4j
Download and install Neo4j (Desktop version 1.6.0 || Neo4j version 5.20.0) from Neo4j Official Download Page  and configure it on your desktop.
Create a database instance with a username and password.
In the project root folder, locate the .env file and update the credentials such as URL, username, and password for accessing the Neo4j instance. This can be a local instance or a Neo4j Aura cloud instance.
Azure OpenAI
Setting Up Environment Variables for Azure OpenAI

To authenticate and interact with Azure OpenAI, configure the following environment variables:
AZURE_OPENAI_API_KEY 	6 API key for authentication.
AZURE_OPENAI_ENDPOINT 	6 Azure OpenAI resource endpoint (e.g., https://your-resource-name.openai.azure.com/ ).
AZURE_OPENAI_DEPLOYMENT 	6 Deployment name for the model (e.g., gpt-35-turbo).
AZURE_OPENAI_API_VERSION 	6 API version (e.g., 2024-02-01).
image.png

Configure Azure OpenAI by adding the following details to the .env file:

image.png

Setup Instructions
Clone the Repository: Use git bash (https://git-scm.com/downloads )
git clone http://engtfs.headquarters.sunviewsoftware.com/tfs/Sunview/KITT/_git/KnowledgeGraph
git pull for latest code.
git checkout -b branch_name for creating a new branch.
Configure the Development Environment
Open the Project in an IDE

Open PyCharm (or any preferred IDE) and load the cloned repository.
Ensure Python 3.10.11 is configured for the project.
Set Up a Virtual Environment

Create a virtual environment using the following command:
python -m venv venv
If using PyCharm, it may automatically create a virtual environment in the project root.
Add the interpreter, to the IDE for package management.
Install Dependencies
Run the following command to install all required dependencies in the virtual environment: pip install -r requirements.txt

Running the FastAPI Application
Use run configuration of the IDE to run the FASTAPI server or use the manual method mentioned below.
Use Uvicorn to start the FastAPI server manually:
uvicorn main:app --reload --host localhost --port 10211
This will expose the API on port 10211 for access. Run it globally by replacing localhost with 0.0.0.0
Upon successful execution, you should see:
INFO: Uvicorn running on http://0.0.0.0:10211 (Press CTRL+C to quit)
Accessing the API Documentation
Swagger UI: http://localhost:10211/docs 
Redoc UI: http://localhost:10211/redoc