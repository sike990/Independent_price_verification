Independent Price Verification (IPV) Dashboard (MS Excel)

Project Overview

This project is an advanced MS Excel dashboard built to simulate the core day-to-day function of a Valuation Control (VCS) analyst: performing an Independent Price Verification (IPV).

The system automates the process of comparing "Trader Marks" (prices from the Front Office) against an independent market data source to find, quantify, and report on pricing discrepancies (variances).

The Business Problem

In any financial institution, the Front Office (Traders) values its own portfolio. A core "control" function, VCS, must independently verify these prices to manage risk, prevent over-valuation, and ensure the bank's financial statements are accurate.

This dashboard is the tool that automates this entire reconciliation and reporting process, allowing a manager to instantly identify the source and scale of pricing risks.

Key Features

Automated Data Consolidation: Dynamically pulls data from three separate "raw data" sources (Trader Marks, Independent Prices, Portfolio Holdings) into a central calculation engine.

Dynamic MTM Variance Calculation: Calculates the precise Mark-to-Market (MTM) dollar variance for every asset in the portfolio ((Official_Price - Trader_Price) * Quantity).

Robust Error Handling: Uses IF logic to intelligently identify and flag assets with missing independent prices, preventing calculation errors.

Interactive Management Dashboard: A high-level summary report that answers key business questions, built on a Pivot Table.

Multi-Level Drill-Down: Allows managers to analyze risk by Asset_Class (e.g., Equity, Fixed Income) and FVH_Level (Level 1, 2, 3), following the logical flow of an investigation.

One-Click Filtering: Fully interactive Slicers and PivotCharts allow any user to easily filter the entire report with a single click.

Visual Risk Alerts: Uses Conditional Formatting to automatically highlight high-risk (negative) variances in red, making them "pop" off the page.

Technical Skills & Functions Demonstrated

XLOOKUP: Used as the primary lookup function to robustly link data from multiple tables. (Superior to VLOOKUP as it is not dependent on column order).

Pivot Tables & PivotCharts: The core of the dashboard, used to instantly summarize thousands of rows of data into a high-level report.

IF Statements: Used to build logical control flags and handle potential data errors gracefully.

Slicers: Implemented to create a user-friendly, interactive dashboard experience for managers.

Conditional Formatting: Applied to the Pivot Table to automatically highlight risk areas.

Data Structuring: Designed a clean and scalable data model by separating raw "source" data from the "calculation" engine and the "presentation" dashboard.

Absolute & Relative References ($): Used to create robust formulas that can be dragged down without breaking references.

Excel File Structure

The workbook is organized into 5 distinct sheets for clarity, scalability, and control:

Trader_Prices (Raw Data): Source of truth for trader marks and descriptive data (Asset_Class, FVH_Level).

Official_Prices (Raw Data): Source of truth for independent VCS (market) prices.

Portfolio_Holdings (Raw Data): Source of truth for asset quantities.

Control_Sheet (Calculation Engine): The "brains" of the project. This sheet consolidates all data via XLOOKUP and performs all row-level calculations (e.g., MTM_Difference).

Dashboard (Presentation Layer): The final, high-level summary for management. Contains the Pivot Table, PivotChart, and Slicers.

How to Use

Update the raw data in the first three sheets (Trader_Prices, Official_Prices, Portfolio_Holdings).

Navigate to the Dashboard sheet.

Right-click the Pivot Table and select "Refresh" to load the new data.

Use the Asset_Class and FVH_Level Slicers to interactively analyze the portfolio's pricing risk.
