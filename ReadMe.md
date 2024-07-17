# Project Setup and Deployment to GitHub
## React, Typescript, Node, Azure Functions

## Frontend Setup

1. **Open Terminal**
2. Create a new project directory:
    ```sh
    mkdir example_project
    ```
3. Navigate into the directory:
    ```sh
    cd example_project
    ```
4. Create a new Vite project:
    ```sh
    npm create vite@latest frontend -- --template react-ts
    ```
    - When prompted: `"create-vite@5.3.0 OKay to Proceed? (Y/n)"`, type `Y`.
    - For more information, read: [Vite Guide](https://vitejs.dev/guide/)
5. Navigate into the frontend directory:
    ```sh
    cd frontend
    ```
6. Install dependencies:
    ```sh
    npm install
    ```
7. Start the development server:
    ```sh
    npm run dev
    ```

## Backend Setup

1. **Download Azure Functions Core Tools**: [Azure Functions Core Tools](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=windows%2Ccsharp%2Cbash)
2. **Open a New Terminal**
3. Navigate to the project directory:
    ```sh
    cd example_project
    ```
4. Create a new API directory and navigate into it:
    ```sh
    mkdir api
    cd api
    ```
5. Create a new Azure Function:
    ```sh
    func new --template "Http Trigger" --name "api" --worker-runtime typescript
    ```
6. Install dependencies:
    ```sh
    npm install
    ```
7. Start the backend server:
    ```sh
    npm start
    ```

## Upload to GitHub

### Step 1: Install Git

Ensure Git is installed on your machine. You can download it from [git-scm.com](https://git-scm.com/).

### Step 2: Configure Git

1. **Open Terminal**
2. Set your Git username:
    ```sh
    git config --global user.name "Your Name"
    ```
3. Set your Git email:
    ```sh
    git config --global user.email "your.email@example.com"
    ```
4. Close the terminal.

### Step 3: Initialize and Commit Your Project

1. **Open Terminal**
2. Navigate to your project directory:
    ```sh
    cd example_project
    ```
3. Initialize a new Git repository:
    ```sh
    git init
    ```
4. Add your files to the repository:
    ```sh
    git add .
    ```
5. Commit your changes:
    ```sh
    git commit -m "Initial commit"
    ```

### Step 4: Create a GitHub Repository

1. **Open Browser**
2. Go to [GitHub](https://github.com)
3. Click on the **New** button or the **+** icon and select **New repository**.
4. Enter a repository name and optional description.
5. Choose between public or private visibility.
6. Click **Create repository**.

### Step 5: Link Your Local Repository to GitHub

1. Add the remote repository URL:
    ```sh
    git remote add origin https://github.com/<<your-username>>/<<your-repo>>.git
    ```
2. Push your changes to GitHub:
    ```sh
    git push -u origin master
    ```
