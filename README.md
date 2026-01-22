# IMDB Analytics with SQL & PL/pgSQL

A single-file SQL project that implements a collection of **views and
functions** over a relational IMDB-style database. The focus is on
writing expressive SQL and PL/pgSQL to answer real analytical questions
about movies, people, genres, ratings, and releases.

## Overview

-   Works entirely inside PostgreSQL\
-   Implements **SQL views**, **SQL functions**, and **PL/pgSQL
    functions**\
-   Queries a structured IMDB dataset (movies, people, roles, ratings,
    regions, genres, etc.)\
-   Designed to support higher-level features like search, analytics,
    and reporting

All logic lives in one file: `ass1.sql`.

## What's implemented

### SQL Views

-   **Top movies by votes**\
-   **Deceased people well-known for recent films**\
-   **Genres with strong average ratings and sufficient volume**\
-   **Regions with above-average runtimes**

### SQL Functions

-   **Regex movie search** with formatted runtime (hours/minutes)\
-   **Year-by-year genre popularity** (years with high release volume)\
-   **Actors who played multiple roles in the same movie**

### PL/pgSQL Functions

-   **Release count lookup** with user-friendly messages\
-   **Cast & crew generator** (formatted natural language output)\
-   **"Must-watch" movies by region/year**, including:
    -   Highest-rated movie(s) per year
    -   Aggregated genres
    -   Aggregated principals
    -   Correct handling of ties and missing data

## Techniques used

-   Complex joins across many tables\
-   Aggregation (`GROUP BY`, `HAVING`, window-like logic)\
-   String aggregation and formatting\
-   Regular expressions in SQL\
-   Deterministic ordering rules\
-   Recursive-style logic in PL/pgSQL\
-   Defensive handling of missing / ambiguous data

## Tech stack

-   PostgreSQL\
-   SQL\
-   PL/pgSQL

This project demonstrates strong database-side problem solving with
minimal reliance on application-layer code.
