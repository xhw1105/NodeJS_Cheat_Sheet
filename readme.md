## Extensions

- Prettier
- DotEnv
- Braket Pair Colourizer
- Javascript (ES6) Code Snippets
- ExpressSnippets
- Material Icon Theme

## package.json

    "scripts":{
        "start": "NODE_ENV=production node server",
        "dev": "nodemon server"
    }

## Items to install

    npm i dotenv express
    npm i -D nodemon

## Set config.env

Create a file *config/config.env*.
Inside it, define environment variable such as:

    NODE_ENV = development
    PORT = 5000

## Load environment variables

    const dotenv = require('dotenv');
    dotenv.config({ path: './config/config.env' });

    const PORT = process.env.PORT || 5000;


## Express code example

    const express = require('express');
    const app = express();
    
    ... (set up port etc.)

    app.listen(PORT, console.log(`Server running in ${process.env.NODE_ENV} mode on port ${PORT}`));

# Run the application

The command to run development mode is

    npm run dev

The command to run production mode is

    npm start
