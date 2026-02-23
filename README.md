# Mutual Fund Search & Popularity Backend (Groww)

This repository documents my work on Groww’s mutual fund filtering and popularity features:

https://groww.in/mutual-funds/filter

## Overview

Worked on migrating mutual fund search and popularity from a Java-based implementation to an Elasticsearch-backed system using Quero, with automated ingestion via Airflow.

The goal was to improve scalability, reduce load on the main database, and allow search behavior changes without backend redeployment.

Note: Source code is proprietary to Groww and cannot be shared.

## My Contributions

- Separated mutual fund data from a global database into a dedicated dataset
- Built Python (Airflow) pipelines to update mutual fund popularity daily using incremental ingestion
- Migrated filters (AMC, category, risk) and sorting logic from Java to Elasticsearch queries
- Integrated search with Quero using dataset ID + query ID, enabling dynamic query updates
- Optimized Elasticsearch queries to reduce search latency
- Worked with frontend to align filtering and sorting behavior

## Tech Stack

- Java, Spring Boot
- Python (Airflow)
- Elasticsearch
- Quero
- SQL

## Impact

- Reduced load on primary database
- Improved search latency (~6%)
- Enabled search logic changes without backend redeployment
- Made system easier to extend for future filters and ranking strategies
