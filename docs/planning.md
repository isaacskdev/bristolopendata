# Project Proposal

## Business Case

### Problem statement

Air pollution is an environmental issue that can affect the health and quality of life of people living in urban areas. Bristol has multiple air-quality monitoring locations that collect information about pollution levels, but accessing and understanding this information may be difficult for members of the public who are unfamiliar with environmental datasets.

The aim of this project is to develop a web-based application called **Bristol Air Quality Explorer**. The application will use data from Bristol Open Data to present air-quality information in a clear and accessible format.

Users will be able to explore monitoring locations, view available pollution measurements, filter information by pollutant and compare measurements between different locations. The application will also use charts and visualisations to make the information easier to understand.

### Business benefits

- **Improved accessibility:** Makes Bristol's air-quality information easier for members of the public to access and understand.
- **Data visualisation:** Presents environmental information through charts and visual representations rather than requiring users to interpret raw datasets.
- **Location comparison:** Allows users to compare available pollution measurements between different monitoring locations.
- **Public awareness:** Helps increase awareness of air pollution and environmental conditions across Bristol.
- **Data exploration:** Allows users to explore the available dataset using search and filtering functionality.

### Options Considered

Several alternative approaches were considered for presenting Bristol's air-quality information.

- **Bristol Open Data website:** Users can access the original datasets through Bristol's existing open-data platform. However, the information may require additional interpretation and filtering to be useful to general users.
- **Static information website:** A basic website could display air-quality information using manually entered data. However, this would require manual updates and would not provide the same level of interaction.
- **Bristol Air Quality Explorer:** A custom web application using the Bristol Open Data API. This option was selected because it allows users to interact with the dataset through searching, filtering, comparing and visualising information.

The selected approach provides the best opportunity to develop an interactive information system while meeting the requirements of the assessment.

### Expected Risks

- **API availability:** The Bristol Open Data API may become temporarily unavailable, preventing the application from retrieving information.
- **Data accuracy:** The application relies on the accuracy and completeness of the information supplied by Bristol Open Data.
- **Incomplete data:** Some monitoring locations may not contain all the measurements required for comparisons or visualisations.
- **Development complexity:** Implementing API requests, filtering and data visualisation may take longer than expected.
- **Browser compatibility:** Differences between web browsers and screen sizes could affect the application's appearance or functionality.
- **Data updates:** Changes to the dataset structure or API could require modifications to the application.

## Context Diagram

<img width="1388" height="480" alt="mermaid-diagram (1)" src="https://github.com/user-attachments/assets/de0a2cdb-c9e0-4239-a396-0022cda94790" />

## Project Scope

The system of interest is Bristol Air Quality Explorer, a web-based application designed to retrieve, process and display air-quality information from Bristol Open Data.

The following features and interactions are included within the project scope:

- A web-based interface developed using HTML5, CSS and JavaScript.
- Retrieving air-quality information from the Bristol Open Data API.
- Displaying an overview of the available air-quality information.
- Displaying available air-quality monitoring locations.
- Searching for specific monitoring locations.
- Filtering measurements using available pollutant categories.
- Displaying measurements associated with selected monitoring locations.
- Comparing available measurements between different monitoring locations.
- Presenting air-quality information through charts and visualisations.
- Handling unavailable data and API errors through appropriate messages.

The following features are outside the scope of the project:

- Creating user accounts or requiring users to log in.
- Allowing users to modify or upload information to Bristol Open Data.
- Collecting new air-quality measurements using physical monitoring equipment.
- Providing medical advice or making health diagnoses based on pollution measurements.
- Developing a mobile application.

The system will be designed for members of the public who want to explore and understand air-quality information across Bristol.

