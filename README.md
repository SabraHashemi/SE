# GeoControl Documentation

This documentation includes details on stakeholders, interfaces, and a comprehensive glossary for the GeoControl system.

---

## Stakeholders

| **Stakeholder**                              | **Role/Description**                                                                 |
|----------------------------------------------|--------------------------------------------------------------------------------------|
| **Administrators (Admins)**                  | Manage users, networks, gateways, and sensors with full control over the system.     |
| **Operators**                                | Handle networks, gateways, sensors, and insert measurements into the system.         |
| **Viewers**                                  | Access data for monitoring and analysis purposes, with read-only permissions.        |
| **Environmental Monitoring Agencies**        | Utilize GeoControl for hydrogeological and environmental tracking and decision-making.|
| **Conservationists and Historians**          | Monitor historical buildings for structural integrity using collected data.          |
| **Residential/Commercial Property Managers** | Optimize indoor environments such as temperature and lighting conditions.            |
| **Software Engineers and Developers**        | Maintain, update, and enhance GeoControl's functionalities and reliability.          |
| **Data Analysts**                            | Process collected measurements for statistical insights and detecting anomalies.      |
| **Emergency Response Teams**                 | Use real-time data from GeoControl to assess risks and coordinate responses to hazards. |
| **Government and Municipalities**            | Fund and use GeoControl to monitor public infrastructure and prevent disasters.       |
| **NGOs and Environmental Researchers**       | Leverage GeoControl data for studies, conservation projects, or disaster relief efforts. |
| **Insurance Companies**                      | Use GeoControl data to assess risks and develop policies for property protection.     |
| **Facility Maintenance Teams**               | Monitor building conditions using GeoControl data to prevent structural issues.       |

---

## GeoControl - Interfaces Documentation

This section provides details about the interfaces used by the actors interacting with the GeoControl system. It includes both physical and logical interfaces to ensure clarity in data flow and interaction.

| **Actor**                | **Physical Interface**                     | **Logical Interface**                                                             |
|--------------------------|--------------------------------------------|----------------------------------------------------------------------------------|
| **Administrators (Admins)**       | Desktop or laptop (web-based system)       | System management dashboard for user, network, gateway, and sensor controls.    |
| **Operators**            | Desktop, laptop, or mobile device          | User interface for managing networks, gateways, sensors, and inputting data.    |
| **Viewers**              | Desktop, laptop, or mobile device          | Read-only interface for viewing and analyzing collected data.                   |
| **Environmental Monitoring Agencies** | Desktop or laptop (web-based system)     | Dashboard for monitoring hydrogeological data and generating reports.           |
| **Conservationists and Historians**     | Mobile device, desktop, or laptop          | Interface for accessing historical building surveillance data.                  |
| **Residential/Commercial Property Managers**    | Mobile device, desktop, or tablet          | Monitoring interface for internal environment (temperature, lighting, etc.).    |
| **Software Engineers and Developers**   | Desktop or laptop                          | Development and debugging interface for system maintenance and updates.         |
| **Data Analysts**        | Desktop or laptop                          | Analytical tools for statistical analysis, outlier detection, and data reports. |
| **Emergency Response Teams**  | Mobile device or tablet                   | Real-time data interface for hazard monitoring and response coordination.        |

---

## GeoControl Glossary

This glossary provides detailed explanations of key terms and concepts related to the GeoControl system. It aims to ensure clarity and understanding for both technical and non-technical audiences.

| **Term**                       | **Definition**                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------|
| **Network**                    | A virtual grouping of gateways that function together as part of a system (e.g., a municipal monitoring network). GeoControl defines these networks in software; they don't exist as physical devices. |
| **Gateway**                    | A physical device that serves as a communication hub, collecting data from sensors and transmitting it to a central system via WiFi or cellular network. Each gateway is identified by a unique MAC address. |
| **Sensor**                     | A small, physical measurement device that records environmental variables such as temperature or light. Sensors send data to their assigned gateway via a serial connection and are identified by a unique MAC address. They record local timestamps based on ISO 8601 standards. |
| **ISO 8601 + Timezone**        | A standardized format for representing dates and times that includes the time zone (e.g., "2025-04-06T01:33+02:00"). This ensures consistent and accurate timestamping across different locations. |
| **UTC (Coordinated Universal Time)** | A universal time standard that does not vary with time zones or daylight saving time. GeoControl converts all sensor timestamps to UTC for storage, ensuring consistency in time-based comparisons and analysis. |
| **Outlier Detection**          | The process of identifying unusual data points that significantly deviate from expected patterns. Outliers could signal issues like equipment malfunctions or environmental anomalies. For instance, a sudden temperature spike might indicate sensor error or a localized event. |
| **Statistical Analysis**       | Using mathematical methods to examine and interpret data. GeoControl computes upper and lower thresholds to assess environmental conditions and trends, aiding in decision-making processes. For example, thresholds could be used to detect unsafe temperature ranges. |
| **Token-Based Authentication** | A security system where access is granted using tokens, which act as unique keys. Each token is associated with a user and their role (Admin, Operator, Viewer), ensuring secure and role-based access. Tokens prevent unauthorized entry into the system. |
| **Admin**                      | A user role with complete control over the GeoControl system. Admins can manage networks, gateways, sensors, and users, as well as configure authentication and permissions. Their role is critical for maintaining system functionality and security. |
| **Operator**                   | A user role responsible for managing networks, gateways, and sensors, and inserting measurement data into the system. Operators ensure the system collects accurate and reliable environmental data. |
| **Viewer**                     | A user role with read-only access to the GeoControl system. Viewers can observe and analyze data but cannot make modifications. Typically suited for analysts or stakeholders needing insights from collected data. |
| **High Reliability**           | A measure of system performance indicating minimal data loss. GeoControl ensures that each sensor loses fewer than 6 measurements per year, maintaining accuracy and reliability for critical monitoring applications. |
| **Hydrogeological Monitoring** | Observing and analyzing environmental variables (e.g., temperature, humidity) in mountain areas to assess risks such as landslides or floods. This helps agencies plan preventive measures and protect lives. For example, data on soil moisture levels might indicate potential landslide threats. |
| **Surveillance of Historical Buildings** | Tracking structural and environmental conditions (e.g., vibrations, temperature) in historical buildings to prevent deterioration. GeoControl supports preservation efforts by providing reliable monitoring data. |
| **Control of Internal Parameters** | Monitoring and managing indoor environmental conditions, such as temperature, humidity, and lighting, to improve comfort, efficiency, and safety in residential and working environments. Examples include ensuring consistent temperature in office buildings or optimal lighting in museums. |
| **Timestamp Conversion**       | The process of changing local timestamps recorded by sensors into UTC for storage. This ensures all collected data is standardized and easily comparable, regardless of its original location. When retrieved, timestamps can be converted back to local time for user convenience. |
| **Role-Based Access**          | A security model that assigns specific permissions to users based on their roles (Admin, Operator, Viewer). Admins have full control, Operators can manage networks and sensors, and Viewers can only access data for observation. This ensures data integrity and prevents unauthorized modifications. |
| **MAC-Based Device**           | A device identified by a unique MAC (Media Access Control) address. This address acts like a digital fingerprint, allowing gateways and sensors to communicate securely within the GeoControl system. |
| **Data Flow**                  | The movement of information through the GeoControl system. For example, sensors collect environmental data every 10 minutes and send it to gateways, which transmit the data to the central system for processing, analysis, and storage. |
| **Central System**             | The core of GeoControl where all data is collected, processed, and stored. It performs key functions like timestamp conversion, outlier detection, statistical analysis, and data visualization for users. |
| **WiFi/Cellular Connection**   | Methods gateways use to communicate with the central system. WiFi is typically used for stable, fixed locations, while cellular connections are ideal for remote or mobile setups. |
| **Serial Connection**          | A direct link between sensors and their assigned gateways for transferring data. This ensures reliable communication in localized monitoring setups. |

---

This updated version ensures consistency across stakeholders, interfaces, and glossary sections. Let me know if further refinements are needed!
