# Microservice that changes Video to Mp3

Small flask microservice that is being orchestrated by Kubernetes in Docker containers that will convert a video to mp3 upon being validated via the Gateway api. Once a video is sucessfully uploaded a message is sent from the Gateway api to a RabbitMQ queue where it can be consumered by the Converter Service which will convert the video that was saved to a MongoDB document to mp3. Upon successfully completing that, it will then return a message to the notification service. The notification service will then notify the user by email that the audio is availabe to download.



## Tech Stack
**language:** Python

**Containerization and Orchestration:** Docker, Kubernetes

**Server:** Flask

**Database:** MongoDB, MySQL
