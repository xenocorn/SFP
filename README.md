# SFP
- [English version](#english-version)  
    - [Protocol purpose](#protocol-purpose)  
    - [Protocol description](#protocol-description)  
- [Русская версия](#русская-версия)  
    - [Назначение протокола](#назначение-протокола)  
    - [Описание протокола](#описание-протокола)  
## English version
### Protocol purpose
SFP(Simple Frame Protocol) is a session layer protocol designed for transmitting data frames over the transport and application layer stream protocols such as TCP, SSL, QUIC, UNIX DOMAIN SOCKET, etc.
To simplify code and save computing resources, SFP is significantly simplified compared to analogues such as WebSocket.
The protocol is intended for use in tasks where high data exchange rates or low overhead are required, such as IoT or message queues and buses.  
### Protocol description
After the connection of the underlying protocol is established, data flows in both directions are used independently of each other.
The protocol has a single packet type consisting of a constant-length header and a variable-length body.
The header contains a single 32-bit unsigned integer value indicating the length of the body.
The protocol does not support PING-PONG packets to support the session, placing this responsibility on the lower or higher protocols.
## Русская версия
### Назначение протокола
Протокол сеансового уровня SFP(Simple Frame Protocol) предназначен для передачи кадров данных поверх поточных протоколов транспортного и прикладного уровня таких как TCP, SSL, QUIC, UNIX DOMAIN SOCKET.  
Для упрощения кода и экономии вычислительных ресурсов SFP значительно упрощен по сравнению с аналогами такими как WebSocket.
Протокол предназначен для использования в областях, где требуется высокая скорость обмена данными или низкие накладные расходы, таких как IoT или очереди и шины сообщений.
### Описание протокола
После установки соединения нижележащего протокола, потоки данных в обе стороны используются независимо друг от друга.
Протокол имеет единственный тип пакета, состоящий из заголовка постоянной длины и тела переменной длины.
Заголовок содержит единственное 32битное беззнаковое целочисленное значение указывающее на длину тела.
Протокол не поддерживает PING-PONG пакеты для поддержки сеанса, возлагая эту обязанность на ниже или вышележащие протоколы.
