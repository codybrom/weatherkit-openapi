# Unofficial WeatherKit REST API OpenAPI Specification

[![Apple WeatherKit](https://img.shields.io/badge/Apple-WeatherKit-blue?logo=apple)](https://developer.apple.com/weatherkit/)
[![Swagger UI](https://img.shields.io/badge/Swagger-UI-85EA2D?logo=swagger&logoColor=black)](https://swagger.io/tools/swagger-ui/)
[![OpenAPI 3.0](https://img.shields.io/badge/OpenAPI-3.0-6BA539?logo=openapi-initiative&logoColor=white)](https://www.openapis.org/)
[![GitHub license](https://img.shields.io/github/license/codybrom/weatherkit-openapi)](https://github.com/codybrom/weatherkit-openapi/blob/main/LICENSE)

An OpenAPI 3 specification for Apple's WeatherKit REST API with interactive Swagger UI documentation.

🔗 **SwaggerUI:** [https://codybrom.github.io/weatherkit-openapi/](https://codybrom.github.io/weatherkit-openapi/)

## Why This Exists

Apple provides a powerful WeatherKit REST API but hasn't published an official OpenAPI/Swagger specification. This project fills that gap by offering:

- Complete API endpoint documentation
- Request/response schema definitions
- Interactive UI for exploring the API structure
- Reference for client code generation

> [!CAUTION]
> **Privacy Note:** The Swagger UI interface runs entirely client-side. Your weather data, coordinates, and JWT tokens never leave your device. Due to CORS restrictions, direct API calls from the Swagger UI won't work - it's designed for documentation purposes only.

## Authentication

All WeatherKit endpoints require JWT authentication with ES256 signature.

```plaintext
Authorization: Bearer <your_jwt_token>
```

For details on generating valid tokens, see [Apple's authentication documentation](https://developer.apple.com/documentation/weatherkitrestapi/request_authentication_for_weatherkit_rest_api).

## API Coverage

This specification covers all endpoints of the Apple WeatherKit REST API:

- Weather data by location (latitude/longitude)
- Current weather conditions
- Daily forecasts
- Hourly forecasts
- Weather alerts
- Historical weather data
- Weather dataset availability

## Usage Examples

### Client Code Generation

You can use this OpenAPI specification to generate client code in various languages:

```bash
# Using OpenAPI Generator
openapi-generator-cli generate -i openapi.yaml -g python -o ./python-client

# Using Swagger Codegen
swagger-codegen generate -i openapi.yaml -l javascript -o ./js-client
```

### API Exploration

The provided Swagger UI lets you explore:

- Available endpoints
- Required parameters
- Expected responses
- Schema definitions

## Contributing

Contributions are welcome! If you notice missing endpoints, incorrect schemas, or other issues:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

Please ensure your changes align with Apple's official documentation.

## Disclaimer

This is an unofficial specification and is not endorsed by or affiliated with Apple Inc. All endpoint specifications are based on Apple's public documentation and may not represent the complete or current API functionality. Always refer to [Apple's official WeatherKit documentation](https://developer.apple.com/documentation/weatherkitrestapi) for the most accurate information.

## License

MIT
