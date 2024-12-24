---
layout: post
categories: [ sustainability]
title:  "History of Building Energy Modelling"
date:   2024-11-01 07:00:00
---

## History of Building Energy Modelling
### Detailed Overview of Building Energy Simulation Models (1990s - 2000s)

### 1. EnergyPlus
- **Overview**: Developed by the U.S. Department of Energy, EnergyPlus is a comprehensive energy simulation program designed for modeling heating, cooling, lighting, ventilation, and other energy flows in buildings.
- **Core Functionality**:
  - Utilizes a heat balance method to calculate energy loads and consumption.
  - Allows for dynamic thermal simulation with time steps of less than one hour, enabling detailed analysis of building performance.
  - Supports modular systems and plant integration, facilitating complex HVAC modeling.
  - Features include:
    - Assessment of passive performance and thermal mass.
    - Calculation of solar gains, surface temperatures, and radiant exchanges.
    - Reporting capabilities for energy consumption, carbon emissions, and room comfort at various intervals (annual, monthly, daily, hourly).
    - Ability to export data for detailed Computational Fluid Dynamics (CFD) analysis.
- **Integration**: Often used in conjunction with user-friendly interfaces like DesignBuilder to simplify model creation and simulation execution.

### 2. eQUEST
- **Overview**: eQUEST is a free software tool that combines sophisticated building energy simulation capabilities with an intuitive interface designed for ease of use across all design phases.
- **Core Functionality**:
  - Built on an advanced version of the DOE-2 engine, providing reliable energy use estimates.
  - Features a building creation wizard and an Energy Efficiency Measure (EEM) wizard to guide users through model setup and analysis.
  - Capable of performing parametric simulations to evaluate various design alternatives quickly.
  - Generates graphical results that highlight energy use patterns and efficiency measures.
- **Applications**: Suitable for both schematic design and detailed analysis phases, allowing users to assess the impact of new technologies on building performance.

### 3. TRNSYS
- **Overview**: TRNSYS (Transient System Simulation Tool) is a flexible software environment used to simulate the behavior of transient systems across various applications beyond just building energy analysis.
- **Core Functionality**:
  - Comprises a kernel that processes input files and iteratively solves system equations to determine convergence.
  - Includes an extensive library of approximately 150 components for modeling different parts of a system (e.g., pumps, HVAC equipment).
  - Allows users to create custom components or modify existing ones, enhancing simulation capabilities.
  - Applications extend to central plant modeling, solar thermal processes, geothermal systems, and more.
- **Strengths**: Known for its versatility in simulating complex interactions within buildings and systems over time.

### 4. DesignBuilder
- **Overview**: DesignBuilder provides a user-friendly interface that integrates tightly with EnergyPlus for detailed building energy modeling while maintaining accessibility for users with varying expertise levels.
- **Core Functionality**:
  - Facilitates the generation of IDF files compatible with EnergyPlus for advanced simulations.
  - Offers a graphical interface that simplifies the definition of building geometry and systems.
  - Provides access to databases of building materials, constructions, and glazing options to streamline model setup.
- **Features**: Users can conduct simulations without extensive knowledge of EnergyPlus's underlying complexities while benefiting from its powerful simulation capabilities.

### 5. OpenStudio
- **Overview**: OpenStudio is an open-source platform developed by NREL that supports parametric modeling and integration with EnergyPlus.
- **Core Functionality**:
  - Offers a graphical user interface via a SketchUp plugin for easy model creation and editing.
  - Supports scripting through Ruby for customization and advanced functionality.
  - Facilitates collaboration by allowing users to share models across different tools within the OpenStudio ecosystem.

### 6. IESVE (Integrated Environmental Solutions Virtual Environment)
- **Overview**: IESVE is a comprehensive suite designed for detailed building energy modeling and optimization across various performance aspects.
- **Core Functionality**:
  - Provides tools for daylighting analysis, thermal comfort assessment, and whole-building performance evaluations.
  - Integrates seamlessly with other IES software modules to enhance overall design efficiency.

### 7. Autodesk Insight
- **Overview**: Autodesk Insight is a cloud-based tool that integrates with Autodesk Revit for advanced energy analysis during the design process.
- **Core Functionality**:
  - Enables early-stage design decisions by evaluating energy performance alongside architectural considerations.
  - Provides insights into building performance metrics such as energy consumption and carbon footprint.

- **Integration into Design Processes**:
  - As sustainability gained traction, energy modeling became integral to architectural design.
  - An integrated design approach fostered collaboration among architects, engineers, and energy modelers to optimize building performance from the outset.

## Regulatory Changes and Standardization (2000s - Present)

### Standard Assessment Procedure (SAP)
- **Overview**: The Standard Assessment Procedure (SAP) was introduced in the UK in 1993 as a standardized method for assessing the energy performance of domestic buildings. It was developed by the Building Research Establishment (BRE) based on the BRE Domestic Energy Model (BREDEM).
  
- **Historical Context**:
  - **1994**: SAP was officially referenced in the UK Building Regulations, solidifying its role in evaluating residential energy performance.
  - **2007**: SAP became the underlying methodology for Energy Performance Certificates (EPCs), which provide essential information about a property's energy efficiency and environmental impact.
  - **2005**: The Reduced Data SAP (RdSAP) was introduced to simplify assessments for existing dwellings, allowing assessors to use predefined assumptions, thus reducing data collection requirements.

- **Revisions and Updates**:
  - SAP has undergone multiple revisions to enhance accuracy and adapt to evolving energy efficiency regulations, with significant updates in **1998**, **2001**, **2005**, **2009**, **2012**, and most recently in **2022**.
  - Each revision has aimed to incorporate advancements in technology, construction practices, and changes in environmental policy.

- **Current Developments**:
  - The UK government is currently developing an enhanced methodology known as the Home Energy Model, aimed at improving accuracy, resilience, and alignment with net zero emissions goals. A consultation was released in December 2023 to gather feedback from stakeholders, with plans for integration into the Future Homes Standard by 2025.

- **Impact on Homeowners**:
  - Compliance with SAP assessments is mandatory for new homeowners. Understanding these requirements is crucial for those involved in building or renovating homes.

### Building Performance Evaluation (BPE)
- **Overview**: The late 2000s saw a growing emphasis on performance-based building codes that require compliance with specific energy performance standards. Building Performance Evaluation (BPE) has become essential for demonstrating compliance with these codes.

- **Definition and Purpose**:
  - BPE involves assessing a building's technical performance regarding energy flows, heat transfer, moisture management, and carbon emissions. It helps identify discrepancies between predicted and actual performance.
  - It provides insights into how buildings operate under real-world conditions, enabling better adaptation measures to improve resilience against climate change.

- **Key Standards and Methodologies**:
  - In 2021, the British Standards Institute launched BS 40101:2021, which was updated in 2022. This standard provides guidance on evaluating building performance based on data gathered from tests, measurements, observations, and user experiences.
  - BPE is considered a form of Post-Occupancy Evaluation (POE) that can be conducted at any point during a building's lifecycle.

- **Importance of Energy Modeling**:
  - Energy modeling has become integral to BPE as it allows designers and builders to estimate anticipated energy consumption based on various design parameters.
  - Compliance modeling predicts a building's energy use against hypothetical baseline models established by codes like IECC and ASHRAE Standard 90.1. This approach enables flexibility in meeting performance specifications while ensuring adherence to regulatory standards.

- **Challenges and Future Directions**:
  - There are challenges associated with discrepancies between predicted and actual energy use due to reliance on standardized assumptions during compliance modeling. This gap can lead to non-compliance with


## Recent Trends and Future Directions (2010s - Present)

- **Whole-Building Life Cycle Assessment**:
  - Recent advancements have broadened energy modeling to encompass embodied energy assessments throughout a building's life cycle.
  - This holistic approach considers materials, construction processes, maintenance, and decommissioning impacts on overall sustainability.

- **Digital Twins and Smart Technologies**:
  - The rise of digital twin technology enables real-time monitoring and optimization of building performance through IoT integration.
  - These virtual replicas facilitate predictive maintenance and enhance operational efficiency.

- **Focus on Historic Buildings**:
  - There is increasing interest in applying energy modeling techniques to historic buildings.
  - Challenges persist regarding predictive model accuracy due to variations in traditional construction methods and materials.
  - Ongoing research aims to refine these models for better assessment of older structures while preserving their historical integrity.

