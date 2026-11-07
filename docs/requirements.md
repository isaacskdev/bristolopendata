# Requirements

## User Needs

### User stories

- As a **Bristol resident**, I want to view air-quality measurements across Bristol so that I can understand pollution levels in my local area.
- As a **website user**, I want to search for and select monitoring locations so that I can find air-quality information for specific areas.
- As a **website user**, I want to filter air-quality information by pollutant so that I can focus on the measurements I am interested in.
- As a **website user**, I want to compare air-quality measurements between different locations so that I can identify differences in pollution levels.
- As a **website user**, I want to view air-quality information through charts and visualisations so that the data is easier to understand.

### Actors

- **Website user:** A member of the public who uses the application to explore Bristol's air-quality information.
- **Bristol Open Data API:** The external data source that provides the air-quality dataset used by the application.
- **Web application:** The system that retrieves, processes and presents the air-quality information to the user.

### Use Cases

### Use Case Diagram

<img width="1168" height="908" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/91a3b451-c702-48c7-8e28-85bda5b5cbec" />

#### UC1 | View Air Quality Dashboard

| | |
|---|---|
| Description | Allow users to view an overview of Bristol's air-quality information using data from Bristol Open Data. |
| Actors | Website user, Bristol Open Data API |
| Assumptions | The user has access to the website and an internet connection is available. The API is accessible. |
| Steps | 1. User opens the website. 2. System requests air-quality data from the API. 3. API returns the available dataset. 4. System processes the data. 5. System displays an overview of the air-quality information. |
| Variations | If the API is unavailable, the system displays an appropriate error message. |
| Non-functional | NFR1, NFR2, NFR3 |
| Issues | The availability and accuracy of the external API may affect the information displayed. |

#### UC2 | Search and View Monitoring Locations

| | |
|---|---|
| Description | Allow users to find and select air-quality monitoring locations to view their associated measurements. |
| Actors | Website user |
| Assumptions | Monitoring location information is available within the dataset. |
| Steps | 1. User navigates to the monitoring locations section. 2. System displays available locations. 3. User searches for or selects a location. 4. System retrieves the associated measurements. 5. System displays the selected location's information. |
| Variations | If no matching location is found, the system informs the user that no results are available. |
| Non-functional | NFR1, NFR2, NFR4 |
| Issues | The search functionality depends on the location information provided by the dataset. |

#### UC3 | Filter Air Quality Data

| | |
|---|---|
| Description | Allow users to filter air-quality information by pollutant to find specific measurements. |
| Actors | Website user |
| Assumptions | The dataset contains identifiable pollutant measurements. |
| Steps | 1. User opens the filtering options. 2. User selects a pollutant. 3. System processes the selected filter. 4. System displays the matching measurements. |
| Variations | If no matching measurements are available, the system displays a message indicating that no results were found. |
| Non-functional | NFR1, NFR2, NFR4 |
| Issues | Available filtering options depend on the pollutants included in the dataset. |

#### UC4 | Compare Air Quality Between Locations

| | |
|---|---|
| Description | Allow users to compare air-quality measurements between different monitoring locations. |
| Actors | Website user |
| Assumptions | The dataset contains comparable measurements for multiple locations. |
| Steps | 1. User opens the comparison section. 2. User selects two or more monitoring locations. 3. System retrieves their available measurements. 4. System compares the selected data. 5. System displays the results in a comparison table or chart. |
| Variations | If insufficient data is available for a selected location, the system informs the user. |
| Non-functional | NFR1, NFR2, NFR4 |
| Issues | Comparisons must use compatible pollutant measurements and units. |

#### UC5 | View Air Quality Visualisations

| | |
|---|---|
| Description | Allow users to view air-quality measurements through charts and visual representations. |
| Actors | Website user |
| Assumptions | Valid measurement data is available for visualisation. |
| Steps | 1. User selects a monitoring location or pollutant. 2. System retrieves the relevant measurements. 3. System processes the data. 4. System generates a chart or visualisation. 5. User views the presented information. |
| Variations | If insufficient data is available, the system displays an appropriate message instead of a chart. |
| Non-functional | NFR1, NFR2, NFR4 |
| Issues | The type of visualisation depends on the structure and availability of the dataset. |

## Software Requirements Specification

### Functional requirements

- **FR1:** The system shall retrieve air-quality data from the Bristol Open Data API. (UC1)
- **FR2:** The system shall display an overview of the available air-quality information. (UC1)
- **FR3:** The system shall display available air-quality monitoring locations. (UC2)
- **FR4:** The system shall allow users to search for monitoring locations. (UC2)
- **FR5:** The system shall display air-quality measurements associated with a selected monitoring location. (UC2)
- **FR6:** The system shall allow users to filter measurements by pollutant. (UC3)
- **FR7:** The system shall update the displayed results when a filter is selected. (UC3)
- **FR8:** The system shall allow users to select multiple monitoring locations for comparison. (UC4)
- **FR9:** The system shall display comparable measurements for the selected locations. (UC4)
- **FR10:** The system shall generate visual representations of the available air-quality measurements. (UC5)
- **FR11:** The system shall display appropriate messages when no matching data is available. (UC1, UC2, UC3, UC4, UC5)
- **FR12:** The system shall display an error message if the API request fails. (UC1)

### Non-Functional Requirements

- **NFR1 – Usability:** The application shall provide a clear and easy-to-use interface that allows users to navigate between different sections and access air-quality information without difficulty. (UC1, UC2, UC3, UC4, UC5)

- **NFR2 – Performance:** The application shall retrieve and display available air-quality information within a reasonable time under normal network conditions. (UC1, UC2, UC3, UC4, UC5)

- **NFR3 – Reliability:** The application shall handle API failures and unavailable data without crashing, displaying appropriate error messages to users. (UC1)

- **NFR4 – Compatibility:** The application shall function correctly on modern web browsers and adapt its layout to different screen sizes. (UC2, UC3, UC4, UC5)

- **NFR5 – Data Accuracy:** The application shall display measurements using the values and units provided by the Bristol Open Data dataset and avoid presenting incomplete or invalid measurements as valid results. (UC1, UC2, UC3, UC4, UC5)

