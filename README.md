# Movie Recommendation System

A full-stack movie recommendation and review platform, built with Spring Boot (REST API + MongoDB) on the backend and React on the frontend.

## Architecture

- **Backend**: Spring Boot REST API backed by MongoDB
  - `Movie` — stores movie metadata (title, release date, IMDB ID, etc.)
  - `Review` — stores user reviews linked to movies
  - Layered architecture: Controller → Service → Repository for both entities
- **Frontend**: React (Create React App) consuming the backend REST API

## Tech Stack

- Java, Spring Boot, Spring Data MongoDB
- MongoDB
- React
- Postman (API testing)
- Lombok

## Project Structure

movie-reviews/
├── movies/ # Spring Boot backend
│ └── src/main/java/dev/nikhil/movies/
│ ├── Movie.java
│ ├── MovieController.java
│ ├── MovieService.java
│ ├── MovieRepository.java
│ ├── Review.java
│ ├── ReviewController.java
│ ├── ReviewService.java
│ └── ReviewRepository.java
└── movie-reviews/ # React frontend
└── src/


## Running locally

**Backend:**
```bash
cd movies
./mvnw spring-boot:run
```
Requires a running MongoDB instance (default connection string in `application.properties`).

**Frontend:**
```bash
cd movie-reviews
npm install
npm start
```

## API Endpoints (example)

- `GET /movies` — list all movies
- `POST /movies` — add a new movie
- `GET /reviews/{movieId}` — get reviews for a movie
- `POST /reviews` — submit a new review

## Notes

This project models a modular, independently testable service boundary between Movie and Review domains, with REST API contracts validated via Postman.
