# IRC Server

A Java-based IRC server implementing core features from RFC 1459 and RFC 2812. Supports multi-client connections, channel management, private messaging, and operator controls over standard IRC port 6667.

## Features

- **Channel Management** -- Create, join, and manage channels with topics, invites, kicks, and user/channel modes
- **Private Messaging** -- Direct one-on-one communication between connected users
- **Operator Controls** -- OPER authentication, KILL, DIE, RESTART, and other administrative commands
- **RFC Command Coverage** -- 25+ implemented commands including JOIN, PART, NICK, PRIVMSG, WHOIS, MODE, LIST, MOTD, and more
- **Concurrent Client Handling** -- Thread-pooled architecture using Java NIO for non-blocking I/O

## Tech Stack

- **Language:** Java
- **Networking:** Java NIO (non-blocking I/O with `ServerSocketChannel`)
- **Concurrency:** `ExecutorService` thread pool
- **Testing:** JUnit 5
- **Build:** IntelliJ IDEA project (`.iml`)

## Getting Started

### Prerequisites

- Java JDK 11 or later

### Build and Run

1. Clone the repository:
   ```
   git clone https://github.com/zachbroad/irc-server.git
   cd irc-server
   ```

2. Compile:
   ```
   javac -d out src/JIRC/*.java src/JIRC/**/*.java
   ```

3. Run:
   ```
   java -cp out JIRC.Main
   ```

   The server starts on `localhost:6667`.

4. Connect with any IRC client:
   ```
   irssi -c localhost -p 6667
   ```

### Configuration

Server settings (hostname, port, operator password) are defined in `IrcServer.java`. The message of the day is loaded from `motd.txt`.

## Implemented Commands

AWAY, DIE, INFO, INVITE, ISON, JOIN, KICK, KILL, LIST, MODE, MOTD, NAMES, NICK, NOTICE, OPER, PART, PING, PRIVMSG, QUIT, RESTART, TIME, TOPIC, USER, WHO, WHOIS

## License

[MIT](https://choosealicense.com/licenses/mit/)
