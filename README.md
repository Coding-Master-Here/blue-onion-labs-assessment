# Setup Guide

This repository contains the Docker Compose setup to run the Assessment, which includes: ✅ A Ruby on Rails backend ✅ A React frontend (TypeScript) ✅ A PostgreSQL database
Project Structure

url-shortner-/
├── blue_onion_labs/  (backend)
├── journal-entries-client/ (frontend)
├── docker-compose.yml
├── README.md
# Prerequisites

Before running the project, ensure you have:

✅  Rails 8.0.2 ✅  Ruby 3.2.2 ✅ Docker installed ✅ Docker Compose installed ✅ Git installed → Download Git ✅ Postgres Installed

# Setup & Installation (using Docker)

Clone the Setup Repository

Clone Backend & Frontend Repositories

git clone https://github.com/Coding-Master-Here/journal-entries-client.git (frontend)

git clone https://github.com/Coding-Master-Here/blue_onion_labs.git (backend)

docker-compose up --build OR sudo docker-compose up -- build

# Setup & Installation (without Docker)

Clone Backend & Frontend Repositories

git clone https://github.com/Coding-Master-Here/journal-entries-client.git (frontend)

git clone https://github.com/Coding-Master-Here/blue_onion_labs.git (backend)

**run the servers manually **

backend ~ rails s
frontend ~ npm run dev


# PostgreSQL Database Setup

Access PostgreSQL CLI

docker exec -it postgres-container psql -U postgres

Create Database

CREATE DATABASE journal_client_database;

Verify the database

\l

 3 Environment Variables Setup

Create a .env file inside url-shortner-backend/ and add the following:

DATABASE_URL="postgresql://postgres:postgres@db:5432/journal_client_database"
