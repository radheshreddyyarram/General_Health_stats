<div align="center">
  <h1>📊 General Health Stats</h1>
  <p>The core data repository and scraping engine powering intelligent health chatbots with dynamic WHO disease data.</p>
  
  [![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
  [![Data](https://img.shields.io/badge/Data-JSON-lightgrey.svg)](https://www.json.org/)
  [![Flask](https://img.shields.io/badge/Flask-Webhooks-black?logo=flask)](https://flask.palletsprojects.com/)
  [![BeautifulSoup](https://img.shields.io/badge/Scraping-BeautifulSoup4-green)](https://www.crummy.com/software/BeautifulSoup/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
</div>

<br />

## 📖 Table of Contents
- [Overview](#-overview)
- [Repository Structure](#-repository-structure)
- [Key Components](#-key-components)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [License](#-license)

---

## 🔍 Overview
**General Health Stats** serves as the primary data backbone and prototyping environment for health-focused conversational agents. It houses critical JSON datasets that map thousands of disease parameters to their respective World Health Organization (WHO) fact sheets. 

Additionally, it contains a suite of Python scripts designed for dynamic web scraping, multilingual translation prototyping, and Dialogflow webhook integration.

## 🗂 Repository Structure
This repository contains a mix of data assets and Python scripts used for various stages of development:
- **Datasets**: `slugs.json`, `disease.json`
- **Webhooks & APIs**: `app.py`, `healthstats.py`
- **Prototyping Scripts**: `Hackathon.py`, `beginner.py`, `full.py`, `health.py`, `al.py`, `out.py`, `vaccine.py`
- **Database Schema**: `health_bd.sql`

## ✨ Key Components

- **🦠 Disease Slugs (`slugs.json`)**: The most critical asset in this repository. A comprehensive mapping of disease names to their exact WHO URL slugs, enabling dynamic factual extraction.
- **🌐 Multilingual Scraping Engine**: Python functions built with `BeautifulSoup` to target specific HTML structures on WHO pages to extract Overviews, Symptoms, Treatments, and Preventative measures dynamically.
- **🛠 Dialogflow Webhooks (`app.py` & others)**: Prototypical Flask applications that demonstrate how to handle intent fulfillment requests from Google Dialogflow, process them, and return formatted responses.
- **💉 Vaccination Logic (`vaccine.py`)**: Scripts dedicated to calculating personalized vaccination schedules (like the Polio vaccine) based on date of birth.

## 🚀 Getting Started

If you wish to run any of the data extraction scripts or webhooks locally:

### Prerequisites
- Python 3.8+
- PostgreSQL (if utilizing `health_bd.sql`)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/radheshreddyyarram/General_Health_stats.git
   cd General_Health_stats
   ```

2. **Install the required Python packages:**
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Usage

### Utilizing the Data
The `slugs.json` file is designed to be hosted and fetched remotely by other applications (like the main Health Chat Bot) to ensure they always have the latest disease mappings without requiring application redeployments.

URL for raw JSON access:
```text
https://raw.githubusercontent.com/radheshreddyyarram/General_Health_stats/main/slugs.json
```

### Running the Webhooks
To test the webhooks locally:
```bash
python app.py
```
*Note: Ensure your environment variables for translation APIs or Dialogflow credentials are set up appropriately depending on the script you run.*

## 📄 License
This project is open-source and available under the standard MIT License.
