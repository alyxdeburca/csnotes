
### Using Python & Javascript with Firebase
- Firebase Database
  - **No**SQL Realtime Database
  - Managed by Google
  - Accessible via the Internet
  - Compatible with Python, Javascript, etc...
  - Data stored in the cloud
  - Multi-User
  - Can handle real-time update etc. Concurrency, Deadlock
  - Some GDPR issues due to location of servers...
  - ... but a fine for simple (educational) data storage and retrieval
### Comparing Firebase and MySQL

- Firebase
  - Firebase is a cloud-based NoSQL database. Data is stored and processed in the cloud
  - Firebase is suitable for real-time application.
  - Firebase is only available on GCP (Google Cloud Platform). It is owned by Google.
  - In Firebase any key/field can be added easily without affecting the existing design.

- MySQL
  - MySQL is a relational database management system (RDBMS)
  - MySQL mostly used for relationaly data and transactions.
  - MySQL installs it anywhere and several clouds provide support managed version of it.
  - MySQL not so flexible design-wise, New Column insertion may affect the design.

|                 | **MySQL**                                  | **Firebase**                              |
|-----------------|----------------------------------------|---------------------------------------|
| **Nature**          | Relational (SQL) database              | Non-relational (NoSQL) database       |
| **Design**          | Based on Tables                        | Based on Collections and Documents    |
| **Scalability**     | Vertical (Rows) Add CPUs, Memory, etc. | Horizontal - Scale-out over a cluster |
| **Model**           | Detailed Model required                | Less detail needed                    |
| **Community**       | Huge Community                         | Smaller but growing                   |
| **Standardisation** | Based on SQL                           | No standard query language            |
| **Schema**          | Rigid Schema                           | Dynamic Schema                        |
| **Flexibility**     | Design is Less Flexible                | Design more Flexible                  |
pg281 Q4

