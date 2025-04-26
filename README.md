# WeatherKit Swagger UI

An OpenAPI 3 spec for Apple’s WeatherKit REST API, rendered with Swagger UI and published via GitHub Pages.

🔗 Live demo: <https://codybrom.github.io/weatherkit-swagger/>

## Usage

1. Clone this repo.
2. Edit `weatherkit.yaml` with your spec.
3. Push to `main` → GitHub Actions will auto-deploy.

## JWT Authentication

All endpoints require `Authorization: Bearer <JWT>` (ES256 signed). See Apple’s docs:
<https://developer.apple.com/documentation/weatherkitrestapi/request_authentication_for_weatherkit_rest_api>
