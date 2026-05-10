# System Architecture: BOSC Community Library (LSDS)

This document outlines the relationship between the data storage and the localization engine of the Local Service Discovery System.

## 1. Data Flow Overview
The system utilizes a decoupled architecture where the resource metadata is separated from the display logic and language strings.

## 2. Component Relationship
* **Central Database (`src/data/database.json`)**: Acts as the "Single Source of Truth." It stores unique IDs, file paths, and category tags.
* **Localization Layer (`src/locales/`)**: Contains language-specific mappings (Swahili, Luganda, English). 

## 3. The Connection Logic
The connection is established via **Category Keys**. 
When a user searches for a resource:
1. The system identifies the `category` (e.g., "Health") from the `database.json`.
2. The UI looks up that specific key within the active locale file (e.g., `lg.json` -> `"health": "Eby'obulamu"`).
3. This ensures that while the data remains static, the user interface remains accessible to the local community.

## 4. Technical Benefits
- **Scalability**: New resources can be added to the JSON database without touching the translation files.
- **Inclusivity**: New local languages can be added by simply creating a new `.json` file in the locales folder.