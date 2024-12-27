# Phonebook

## Prerequisites

Before running the project, follow these steps:

### 1. Install Dependencies

In the terminal, at the root of the project, run the following command to install all the necessary dependencies:

#npm install

### 2. Install & run json server

Before running the Angular application, make sure that json-server is running. If you don't have json-server installed globally, use the following command to install it:

npm install -g json-server

### 3. Configuration

After installing json-server, open the src/environments/environment.ts file and check that the api_url is configured to point to your json-server. It should look like this:

export const environment = {
production: false,
api_url: 'http://localhost:3000/'
};

### 4. Run json-server

Navigate to the src/app/services folder where the db.json file is located. From this location, run the following command to start json-server:

json-server --watch src/app/services/db.json --port 3000

This will start json-server on port 3000 and it will watch the db.json file for any changes.

If you choose to run json-server on a different port, make sure to update the api_url in environment.ts to match the new port.

### 5. Run Angular app

Once json-server is running, you can finally start the Angular application. In a new terminal window, navigate to the root of the project and run the following command:

ng serve
