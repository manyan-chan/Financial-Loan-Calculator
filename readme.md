# Financial Loan Calculator

A dynamic and interactive web-based tool designed to help users calculate, visualize, and compare financial loan scenarios, such as mortgages, car loans, or personal loans. Built with HTML, Tailwind CSS, and Chart.js.


<!-- Optional: Add a link to a live demo if you deploy it -->
<!-- [Live Demo](your-live-demo-link-here) -->

<!-- Optional: Add a screenshot -->
<!-- ![Screenshot of the Loan Calculator](path/to/screenshot.png) -->

## Description

This calculator provides a user-friendly interface to input loan parameters like amount, interest rate, and term using intuitive sliders. It instantly calculates the monthly payment, total principal, total interest, and estimated payoff date.

Key features include the ability to factor in extra monthly payments to see how they impact the total interest paid and loan duration, visual representations of the payment breakdown and amortization schedule using interactive charts, and a comparison tool to save and contrast different loan setups side-by-side.

The application is fully responsive and supports both light and dark color schemes based on user system preferences, ensuring a comfortable viewing experience on any device.

## Features

*   **Interactive Loan Inputs:** Sliders for Loan Amount, Annual Interest Rate, and Loan Term (in years).
*   **Extra Payment Simulation:** Toggle and slider to include additional monthly principal payments.
*   **Real-time Calculation:** Instant updates to all results as input parameters change.
*   **Comprehensive Summary:** Displays calculated Monthly Payment, Total Principal, Total Interest, Total Payments, and estimated Payoff Date.
*   **Savings Calculation:** Shows potential Interest Saved and Time Saved when making extra payments.
*   **Payment Breakdown Chart:** Doughnut chart visualizing the proportion of Principal vs. Total Interest over the life of the loan (standard term).
*   **Amortization Chart:** Line chart illustrating the decrease in loan balance over time, comparing standard payments vs. payments with extra contributions.
*   **Detailed Amortization Table:**
    *   Shows year-by-year (or month-by-month) breakdown of principal paid, interest paid, and remaining balance.
    *   Toggle between Yearly aggregate view and Detailed monthly view (first year shown in detailed for brevity, switching to yearly shows all).
    *   Toggle to display a comparison column showing the remaining balance if extra payments were made.
*   **Loan Comparison Tool:**
    *   Save current loan parameters as a scenario.
    *   View multiple saved scenarios in a comparison table.
    *   Load a saved scenario back into the calculator inputs.
    *   Remove saved scenarios.
*   **Responsive Design:** Adapts layout for different screen sizes using Tailwind CSS.
*   **Dark Mode Support:** Automatically detects and applies system's light/dark theme preference, including chart styles.
*   **Tooltips:** Helpful hints explaining input fields and results.

## Technologies Used

*   **HTML5:** Structure and content of the web page.
*   **Tailwind CSS v3 (CDN):** Utility-first CSS framework for styling and responsive design.
*   **JavaScript (ES6+):** Core logic for calculations, DOM manipulation, event handling, and chart integration.
*   **Chart.js v4+ (CDN):** Library for creating interactive and responsive charts.

## Getting Started

No complex setup is required as the application uses CDN links for dependencies.

1.  **Download or Clone:**
    *   Download the `index.html` file.
    *   OR Clone the repository: `git clone <repository-url>`
2.  **Open:**
    *   Navigate to the downloaded file location.
    *   Open the `index.html` file directly in your preferred web browser (e.g., Chrome, Firefox, Safari, Edge).

## Usage

1.  **Adjust Loan Parameters:** Use the sliders for "Loan Amount", "Interest Rate (%)", and "Loan Term (Years)". The values update instantly in the display boxes next to the labels.
2.  **View Summary:** Observe the "Payment Summary" section on the right for the calculated "Monthly Payment", "Total Interest", "Total Payment", and "Payoff Date".
3.  **Simulate Extra Payments:**
    *   Locate the "Extra Payments" section below the main parameters.
    *   Toggle the "Include" switch to enable extra payments.
    *   Adjust the "Monthly Extra Payment" slider.
    *   Observe the updated "Payment Summary" (payoff date might change) and the "With Extra Payments You Save" box showing interest and time saved.
4.  **Analyze Charts:**
    *   **Payment Breakdown:** See the ratio of total principal to total interest paid over the standard loan term.
    *   **Amortization:** Track how the loan balance decreases over the years. If extra payments are enabled, a second line shows the faster payoff trajectory. Hover over the chart for specific balance details per year.
5.  **Explore Amortization Schedule:**
    *   Scroll down to the "Amortization Schedule" table.
    *   By default, it shows a yearly summary. Click **"Detailed View"** to see a month-by-month breakdown (limited view for brevity, switch back to yearly for full scope).
    *   If extra payments are enabled in the calculator, click **"Show Savings"** to add a column comparing the year-end balance with and without extra payments. Click **"Hide Savings"** to remove it.
6.  **Compare Scenarios:**
    *   Adjust the loan parameters (including extra payments) to set up a scenario you want to save.
    *   Click the **"Save Current Settings"** button in the "Loan Comparison" section. The current setup will be added as a row in the table below.
    *   Repeat this process to save multiple scenarios.
    *   In the comparison table:
        *   Click the **Trash Can** icon to remove a scenario.
        *   Click the **Refresh** icon to load a scenario's parameters back into the main calculator sliders and inputs.

## Code Structure

All the code (HTML, CSS, JavaScript) is contained within the single `index.html` file for simplicity.

*   **`<head>`:** Contains meta tags, title, CDN links for Tailwind CSS and Chart.js, and inline `<style>` for custom CSS (slider styling, tooltips, etc.) and Tailwind configuration.
*   **`<body>`:** Contains the HTML structure for the header, calculator inputs, results display, charts, and tables, organized using Tailwind CSS grid and flexbox utilities.
*   **`<script>` (at the end of `<body>`):** Contains all the JavaScript logic:
    *   Dark mode detection and handling.
    *   Chart initialization and update functions.
    *   Slider update logic.
    *   Core loan calculation functions (`calculateAndUpdateUI`, `calculateAmortizationSchedule`).
    *   Amortization table generation logic.
    *   Comparison scenario management (add, remove, load).
    *   Event listeners for user interactions.
    *   Utility functions (formatting, date calculation).

## Potential Future Enhancements

*   Add input fields for Property Taxes and Home Insurance (PITI calculation for mortgages).
*   Include an option for a Down Payment.
*   Implement different loan types (e.g., Interest-Only).
*   Persist saved comparison scenarios using `localStorage`.
*   Add functionality to export the Amortization Schedule (e.g., to CSV).
*   Implement more robust input validation with user feedback.
*   Add unit tests for calculation functions.
*   Refactor JavaScript into separate modules for better organization.
*   Add a manual Dark/Light mode toggle button.
