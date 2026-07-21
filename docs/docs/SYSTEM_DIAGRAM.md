# Nexus System Diagram

```text
                   +----------------------+
                   |        User          |
                   +----------+-----------+
                              |
                              |
                     HTTPS Request
                              |
                              ▼
                  +----------------------+
                  |      Frontend        |
                  |      Next.js         |
                  +----------+-----------+
                             |
                    REST API |
                             ▼
                  +----------------------+
                  |      Backend         |
                  |      NestJS          |
                  +----+-----------+-----+
                       |           |
         PostgreSQL    |           | Blockchain
                       |           |
                       ▼           ▼
              +--------------+   +----------------+
              | PostgreSQL   |   | Ethereum/      |
              | Database     |   | Polygon        |
              +--------------+   +----------------+
                       |
                       |
                       ▼
                Activity Logs

                  +----------------------+
                  |     AI Service       |
                  |     OpenAI API       |
                  +----------------------+
```
