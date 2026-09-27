# Taiwan Healthcare Access Dashboard

**Live dashboard:** https://jill-chiou.github.io/taiwan-healthcare-access-dashboard/

An interactive, English-language dashboard of village-level healthcare accessibility in Taiwan (2024).

## What it shows

Taiwan usually ranks healthcare resources by county-level physician density. By that metric, rural Hualien ranks 3rd nationally. This project measures access instead: how much physician supply each of Taiwan's 7,616 villages can actually reach by road.

- **Method:** Enhanced Two-Step Floating Catchment Area (E2SFCA) with a four-zone distance decay (0–10–20–30–60 min)
- **Travel times:** 18.1 million village–facility drive-time pairs from a self-hosted OSRM routing engine on the OpenStreetMap road network
- **Finding:** 96 high-risk villages. 82 of them combine low access with a large elderly population, and all 82 sit in townships that are *not* officially remote, on the fringes of urbanized counties such as Taoyuan, Miaoli, Hsinchu and Keelung. The other 14 have no physician within 60 minutes, all in mountain indigenous townships.

## About this repository

This repository only hosts the static dashboard (`index.html` + pre-computed `dashboard_data.js`). The data pipeline, geocoding, routing and statistical analysis live in a separate private repository.

**Data sources:** Ministry of Health and Welfare (medical facilities and physicians, 2024-12-31), Ministry of the Interior (village population by age, 2024), National Health Insurance Administration, National Land Surveying and Mapping Center (village boundaries), OpenStreetMap contributors (road network).

**Author:** Wei-Chi (Jill) Chiou
