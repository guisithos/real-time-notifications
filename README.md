💡 How It Works:
    User Identification: The system fetches user IDs from incoming requests and verifies their existence.
    Notification Creation: Constructs notifications with user details and the message content.
    Kafka Integration: Marshals notifications into JSON format and sends them to the Kafka topic notifications using a Kafka producer.
    REST API with Gin: Exposes an endpoint /send using the Gin framework to handle incoming notification requests.

🛠️ Technologies Used:
    Go (Golang): For backend logic and API development.
    Apache Kafka: For distributed messaging and real-time communication.
    Gin Framework: For building a performant and easy-to-use REST API.
    Sarama Library: To interface with Kafka from Go.

🔪 How-to-use
    cd to producer folder, and run the producer.go, then cd to the consummer folder and run the consummer.go
    with both running, curl to "curl -X POST http://localhost:9090/send \-d "fromID=2&toID=1&message=Guilherme started following you."
    to retrieve a notification, you can curl "curl http://localhost:9091/notifications/1"
