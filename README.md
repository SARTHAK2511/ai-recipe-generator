
# AI Recipe Generator

AI Recipe Generator is a web application that allows users to generate unique recipes based on a list of ingredients using AI capabilities. This project is built with AWS Amplify for deployment and backend management, and AWS Bedrock for AI-powered recipe generation.

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
```

## Getting Started

### Prerequisites

- **Node.js**: Ensure Node.js is installed. [Download Node.js](https://nodejs.org/)
- **AWS Account**: You'll need an AWS account to deploy resources using AWS Amplify and Bedrock.

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/ai-recipe-generator.git
   cd ai-recipe-generator
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Configure AWS Amplify**:

   Make sure you have configured AWS Amplify CLI with your credentials:

   ```bash
   npm install -g @aws-amplify/cli
   amplify configure
   ```

4. **Deploy the Backend**:

   ```bash
   amplify init
   amplify push
   ```

5. **Run the Application**:

   ```bash
   npm start
   ```

### AWS Amplify Configuration

Ensure that your `amplify_outputs.json` file is correctly generated and included in the project. This file contains the necessary configuration for AWS Amplify to connect your app with the cloud resources.

### AWS Bedrock Configuration

The application queries AWS Bedrock via the `bedrock.js` handler. Ensure your Bedrock data source (`bedrockDS`) is properly configured in AWS Amplify and has the correct permissions and API keys.

## Usage

1. **Open the Application**: After starting the app, open [http://localhost:3000](http://localhost:3000) in your browser.
2. **Login/Signup**: Authenticate using the built-in user authentication.
3. **Generate a Recipe**: Enter a list of ingredients separated by commas and click "Generate".
4. **View Results**: The AI-generated recipe will be displayed on the screen.

## Troubleshooting

- **Common Errors**:
  - *Module 'react' has no exported member 'useState'*: Ensure that `react` and `react-dom` are properly installed and up-to-date.
  - *Code.js:39:11: Uncaught TypeError: Cannot read property '0' of undefined*: This error typically occurs due to an unexpected response from the AI model. Double-check your Bedrock API configuration and data handling.

- **Refreshing AWS SSO**:
  If you encounter a "Token is expired" error, refresh your AWS SSO session:

  ```bash
  aws sso login
  ```

  Then configure the Amplify profile again:

  ```bash
  npx amplify configure profile
  ```

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any suggestions or bug reports.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- **AWS Amplify** for seamless backend integration.
- **AWS Bedrock** for AI-powered recipe generation.
- **React** for a robust frontend framework.
