 Chat-app-project

Here's a high-level project document focusing on the "Keep Update" page feature, with an emphasis on backend and networking:



 Section 1 - Project Description

 1.1 Project
Project Name: Keep Update Widget

 1.2 Description
The "Keep Update Widget" project is designed to allow users to share live updates from their day, including images, videos, and texts, with their friends. These updates will be displayed as a widget on friends' home screens, providing a real-time glimpse into each other's activities.

 1.3 Revision History
| Date       | Comment           | Author   |
|------------|-------------------|----------|
|            | Initial draft     |          |



 Section 2 - Overview

 2.1 Purpose
The purpose of this module is to implement the backend and networking components for the "Keep Update" feature. It is aimed at users who want to share and stay updated with friends' daily activities in real-time.

 2.2 Scope
Included:
- Backend development for user authentication, update management, and media handling.
- Networking setup for real-time updates.
- Data storage and retrieval for updates.

Excluded:
- Frontend GUI development (to be addressed later).
- Advanced analytics or data processing features.
- Integration with other social media platforms.

 2.3 Requirements

 2.3.1 Functional Requirements
- R1: The system shall allow users to register and log in.
- R2: The system shall enable users to post updates including images, videos, and texts.
- R3: The system shall push updates to friends' widgets in real-time.
- R4: The system shall allow users to view a history of updates.

 2.3.2 Non-Functional Requirements
- Performance: The system shall handle up to 1000 concurrent users posting updates.
- Reliability: The system shall have 99.9% uptime and ensure data consistency.

 2.3.3 Technical Requirements
- Hardware: The system shall run on cloud-based servers with scalable resources.
- Software: The backend shall be developed using a modern programming language (e.g., Python, Java) with appropriate frameworks for networking and media handling.

 2.3.4 Security Requirements
- Authentication: Secure user authentication using OAuth 2.0.
- Data Encryption: All data, including media, shall be encrypted in transit and at rest.

 2.3.5 Estimates
| #  | Description                            | Hrs. Est. |
|----|----------------------------------------|-----------|
| 1  | User authentication module             | #         |
| 2  | Update management system               | #         |
| 3  | Media handling and storage             | #         |
| 4  | Real-time update push system           | #         |
| 5  | Database design and implementation     | #         |
|    | **TOTAL:**                             | #         |

 2.3.6 Traceability Matrix
| SRS Requirement | SDD Module                              |
|-----------------|-----------------------------------------|
| Req 1           | 5.1.1 (link to module), 5.1.2 (link)    |



 Section 3 - System Architecture

 3.1 Overview
The system architecture consists of a backend server responsible for managing user authentication, update handling, and media storage. It includes real-time networking components to push updates to users' widgets.

 3.2 Architectural Diagrams
1. Component Diagram: Backend server, database, media storage, real-time communication service.
2. Sequence Diagram: User posting an update, server processing, and pushing the update.
3. Data Flow Diagram (DFD): Flow of data from user input to storage and dissemination.



 Section 4 - Data Dictionary

| Table | Field     | Notes                                  | Type    |
|-------|-----------|----------------------------------------|---------|
| User  | ID        | Unique Identifier                      | DECIMAL |
| User  | Username  | User's display name                    | VARCHAR |
| Update| UpdateID  | Unique Identifier for the update       | DECIMAL |
| Update| MediaType | Type of media (image/video/text)       | VARCHAR |
| Update| Content   | Content URL or text                    | VARCHAR |



 Section 5 – Data Design

 5.1 Persistent/Static Data
5.1.1 Dataset
Entities:
- User:
Attributes: UserID (PK), Username, Password, Email
Relationships: One-to-Many with Updates

Update:
 Attributes: UpdateID (PK), UserID (FK), MediaType, Content, Timestamp


 Section 6 - User Interface Design

This section will be developed later, focusing on the backend and networking components for now.



 Section 7 - Testing

7.1 Test Plan Creation
The test plan focuses on validating the backend and networking functionalities, ensuring that updates are correctly stored, processed, and delivered.

 Components of a Test Plan:
Objective: Ensure the system can handle user registrations, updates, and real-time delivery.
Scope:Backend and networking only.
Resources:Testing tools, simulated load tests.
Schedule: Based on backend development milestones.
Test Cases: Verify user registration, update creation, and delivery.

Test Environment: 
| Test Case | Input               | Expected Output         | Actual Output |
|-----------|---------------------|-------------------------|---------------|
| 1         | User registration   | Successful registration |               |
| 2         | Post update         | Update stored and sent  |               |



Section 8 - Monitoring

The monitoring plan will include:
Performance Metrics: Response times, update processing times, server load.
Error Metrics: Failed update deliveries, authentication errors.
Availability Metrics: System uptime, downtime incidents.



 Section 9 - Other Interfaces

 9.1 External Media Storage Service
Details about interactions with external storage services for handling media uploads and retrievals.



Section 10 - Extra Design Features / Outstanding Issues

Consider implementing content moderation for uploaded media.
Explore scalability options for real-time update pushing.



 Section 11 – References

 OAuth 2.0 documentation
 Cloud storage best practices


 Section 12 – Glossary
 
OAuth 2.0: An open standard for access delegation.
Widget: A small application that displays information or provides a function.

