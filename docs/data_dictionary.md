# 📘 Data Dictionary (Template)

This document provides a reusable structure for describing each variable (column) in your dataset.

> ⚠️ **This is a template**. Replace all placeholder content with information specific to your dataset.

---

## 📑 Structure

Each entry should include:

- **Name**: The variable name (as it appears in the dataset)
- **Type**: The data type (see examples below)
- **Description**: What the variable means
- **Sample Values**: Examples of possible or observed values
- **Valid Range / Categories**: If applicable, expected range or allowed values

---

## 🧾 Example Entries

### Variable 1

- **Name**: `household_id`
- **Type**: Integer
- **Description**: Unique identifier for each household
- **Sample Values**: 101, 102, 103
- **Valid Range / Categories**: Positive integers

### Variable 2

- **Name**: `region`
- **Type**: Categorical (String)
- **Description**: Geographic region where the household is located
- **Sample Values**: "North", "South", "Central"
- **Valid Range / Categories**: One of ["North", "South", "Central"]

### Variable 3

- **Name**: `income`
- **Type**: Float (Continuous)
- **Description**: Reported monthly household income in USD
- **Sample Values**: 850.50, 1200.00, 430.75
- **Valid Range / Categories**: 0 - 10,000

### Variable 4

- **Name**: `has_electricity`
- **Type**: Boolean
- **Description**: Whether the household has access to electricity
- **Sample Values**: True, False
- **Valid Range / Categories**: True or False

---

## 📂 Common Data Types for Reference

- **Integer**: Whole numbers (e.g., 1, 42)
- **Float**: Decimal numbers (e.g., 3.14, 7500.99)
- **String**: Free text or categorical labels (e.g., "Urban", "Yes")
- **Boolean**: True/False values
- **Date**: ISO 8601 formatted date (e.g., "2025-08-07")
- **Categorical**: Enum or finite set of string/int values

---

## ✍️ Reuse Instructions

- Duplicate a block for each variable in your dataset.
- Replace placeholder text with dataset-specific information.
- You can remove or rename fields depending on the structure of your data.
