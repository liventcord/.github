## What is LiventCord?
LiventCord is an open-source, self-hosted communication platform for real-time messaging, channel management, file sharing, and voice/video communication. It prioritizes data security and user privacy.


## Why LiventCord?
LiventCord eliminates the need to rely on third-party services, ensuring your data stays in your hands. By being self-hosted, it offers you more privacy and control over your communication, without depending on external providers or compromising your information.

## Feature

- **Guild & Channel Management**: Create, join, and manage guilds and channels.
- **Messaging**: Send, receive, and delete messages with rich formatting, mentions, reactions, and emoji support.
- **Friendship & Invitations**: Manage friends and invite users to guilds.
- **File Sharing**: Upload and retrieve various file types (images, videos, documents, etc.).
- **Direct Messaging**: 1-on-1 messaging with real-time updates.
  

## Backend 
Built with .NET Core for performance and scalability.

## Database 
Uses Entity Framework Core for database management, supporting a variety of databases:

- **MongoDB**
- **PostgreSQL**
- **MySQL**
- **MariaDB**
- **SQLite**


## Getting Started

To get started with **LiventCord**, you can set up the server locally

### Prerequisites

- **.NET Core SDK**

### Clone the Repository

    $ git clone --depth 1 https://github.com/liventcord/liventcord
---
### Set Environment Variables

1. Create the `Properties/appsettings.json` file in project directory.
2. Add the following JSON configuration and replace placeholders:

    ```json
    {
      "ConnectionStrings": {
        "RemoteConnection": "Host=host;Database=database;Username=username;Password=password;Port=port;SSL Mode=sslmode",
        "SqlitePath": "Data Source=Data/<Database-name>.db",
        "isPostgres": "true/false",
      },
      "AppSettings": {
        "SecretKey": "Secret-Key"
      }
    }
    ```
---
### Run the Server

    $ dotnet run

---

### Future Ideas
- **Voice & Video**: Real-time group and direct voice/video chat.
- **Custom Presence**: Set status with custom messages to reflect availability or activity
- **Search**: Text search to retrieve past conversations
-  **Moderation**: Fine-grained moderation over guild and channel management
-  **SSE Events**: Realtime event streaming

  
### Contributing

Feel free to fork the repository and submit pull requests. We welcome contributions and improvements.

### License

This project is licensed under the GNU General Public License v3.0
