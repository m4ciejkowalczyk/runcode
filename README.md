# E-Commerce Deployment & Analytics (PrestaShop)

## Overview
Web-shop project for the "Electronic Business" course at the Technical University of Gdańsk. The shop is based on PrestaShop 1.7.8 and utilizes data scraped from brooks-running.pl. The project simulates a production-ready e-commerce deployment, featuring automated data migration, containerized infrastructure, UI testing, and business analytics integration.

*Note: This was a collaborative team project. The complete repository is hosted here: https://github.com/KacperZuck/RunCode.*

## My Role & Contributions
I was responsible for the data architecture, automated initialization, and business analytics integration. My key deliverables included:

* **Custom Web Scraper:** Developed an automated scraping tool to extract a massive dataset from an existing online store. The script successfully gathered over 300 real products, preserving complex attributes (e.g., categories, subcategories, prices, physical dimensions, product variants, and high-resolution images).
* **REST API Data Seeding:** Instead of manual database entry, I engineered a dedicated script utilizing the PrestaShop REST API. This script parsed the scraped dataset and automatically initialized the store's inventory, recreating the exact category trees and product relationships in the new PrestaShop instance.
* **Google Analytics & Event Tracking:** Fully integrated Google Analytics with e-commerce tracking capabilities. I configured metric tracking, including:
  * **Destination Goals:** Tracking successful user account registrations.
  * **Custom Event Tracking:** Implementing custom JS triggers to monitor user interactions with promotional banners and tracking when discounted items were added to the shopping cart.
* **Store Configuration:** Adjusted core PrestaShop settings to meet specific business requirements. This included configuring regional settings, setting up email notifications, and implementing complex shipping logic (e.g., free shipping for orders over 2,000 PLN, and blocking delivery for carts exceeding 50 kg).

## Key Team Achievements (Overall Project Scope)
While my focus was on data and analytics, as a team we successfully implemented:
* **Containerized Infrastructure:** Deployed on a student cluster using `Docker` and `docker-compose` with isolated database and web server instances.
* **Automated UI Testing:** Selenium scripts capable of executing a full user journey (searching, adding to cart, registering, ordering, and downloading invoices) in under 5 minutes.
* **Security:** Enforced HTTPS with custom SSL certificates.

## Technologies Used
* **CMS / Backend:** PrestaShop 1.7.8, REST API, PHP
* **Data Extraction:** Python, BeautifulSoup, Selenium
* **Analytics:** Google Analytics, Custom JS Event Listeners

