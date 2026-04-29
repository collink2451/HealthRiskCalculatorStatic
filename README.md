# Health Risk Calculator

Static frontend for a health insurance risk calculator. Collects four health factors from the user and displays an overall risk tier in real time, powered by the [health-risk-calculator-api](../health-risk-calculator-api) backend.

## Features

- **Age** — scored into risk points based on age group
- **BMI** — calculated from height (inches) and weight (lbs), classified as normal, overweight, or other
- **Blood Pressure** — systolic/diastolic classified by AHA stages
- **Family Diseases** — checkboxes for Diabetes, Cancer, and Alzheimer's (10 points each)
- Color-coded risk indicators update on every input change
- Overall risk tier: Low Risk / Moderate Risk / High Risk / Uninsurable

## Tech Stack

- Vanilla HTML, CSS, JavaScript
- Bootstrap 5 (dark theme)
- jQuery
- Calls [health-risk-calculator-api](../health-risk-calculator-api) for all calculations

## Setup

No build step required. Serve with any static file server:

```bash
npx serve .
# or
python -m http.server 8080
```

The API URL is hardcoded in `assets/scripts.js` — update it if running the API locally:

```js
const api_url = "http://localhost:3000";
```

## Deployment

No build step required — deploy the directory as-is to any static hosting provider or web server.
