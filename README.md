# Kolas.Ai Public API - OpenAPI Specification

Welcome to the **Kolas.Ai Public API** documentation! This repository hosts the OpenAPI 3.1 specification for Kolas.Ai's public API, making it easy for developers to integrate Kolas.Ai’s machine learning services into their applications.

## Overview

The Kolas.Ai API is designed to classify message categories based on a trained dataset within a configured project. Use this API to accurately categorize messages into types like "Neutral," "Insult," or "Spam."

### Key Features
- **Predict Message Categories**: Use the `/predictions/predict` endpoint to classify messages based on your project-specific dataset.
- **High Accuracy**: Predictions include probability scores, giving you confidence in the classification results.
- **OAuth2 Authentication**: Secure access via OAuth2 client credentials flow.

## Usage

The Kolas.Ai API follows the OpenAPI 3.1 standard, which enables easy exploration and integration with various tools. To get started:

1. **Authentication**: Obtain an access token using OAuth2 client credentials.
2. **Make Predictions**: Send a POST request to `/predictions/predict` with your `projectId` and messages.
3. **Receive Predictions**: Retrieve predicted categories and their probabilities in the API response.

## Authentication

This API uses **OAuth2 client credentials** for secure access. You’ll need to request a token using your client credentials from the Kolas.Ai platform.

### Example Request
Once you have your access token, you can make a request like this:

```json
{
  "projectId": 3457,
  "messages": [
    { "message": "How was your day?" }
  ]
}
```

### Example Response

The response includes predictions and associated probabilities:

```json
{
  "predictions": [
    {
      "categories": ["Neutral", "Insult", "Spam"],
      "prediction": "Neutral",
      "probability": "0.998",
      "message": "How was your day?"
    }
  ]
}
```

## Documentation Links
- [Swagger Documentation](https://swagger.io/): Explore the OpenAPI specification.
- [Kolas.Ai Platform Documentation](https://kolas.ai/documentation): Learn more about configuring projects and using Kolas.Ai’s platform.

## License

This API specification is released under the **Apache 2.0 License**. See the [LICENSE](https://www.apache.org/licenses/LICENSE-2.0.html) for more details.

__

Feel free to explore, test, and integrate Kolas.Ai's API, and reach out with any questions!