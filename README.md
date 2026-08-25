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
