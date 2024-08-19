# AI Recipe Generator

AI Recipe Generator is a web application that allows users to generate unique recipes based on a list of ingredients using AI capabilities. This project is built with AWS Amplify for deployment and backend management and AWS Bedrock for AI-powered recipe generation.

## Features

- **Ingredient-based Recipe Generation**: Input a list of ingredients, and the AI will generate a custom recipe.
- **User Authentication**: Secure login and session management.
- **AWS Amplify Integration**: Deployed and managed using AWS Amplify.
- **AI-Powered by AWS Bedrock**: Uses AWS Bedrock for generating recipes based on user input.

## Project Structure

```plaintext
├── amplify/              # AWS Amplify backend configuration
├── public/               # Public files
├── src/                  # Source code
│   ├── components/       # React components
│   ├── App.tsx           # Main application file
│   ├── amplify_outputs.json  # Amplify output configuration
│   └── bedrock.js        # AWS Bedrock query handler
├── .gitignore            # Git ignore file
├── README.md             # Project documentation
└── package.json          # Node.js dependencies and scripts
