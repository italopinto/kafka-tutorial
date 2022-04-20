# Kafka-dockerized
Tutorial on how to dockerize kafka. From [better data science](https://www.youtube.com/watch?v=4xFZ_iTZLTs&list=PLQ5j-FTc2VhAY_PBg7FVkZsal50MCgp7Y) YouTube channel.

## How to test
- First of all, run `docker-compose -f docker-compose.yml up -d`, if you don't have docker installed follow the Docker official documentation: https://docs.docker.com/engine/install/
- Then, there is three python files in the `kafka-python-code` folder.
- The first `consumer.py` is the Kafka consumer.
- The sencond `data_generator.py` is the dummy data generator to producer data to the topic `messages` in Kafka.
- The third `producer.py` is the Kafka producer, it uses the `data_generator.py`.
### To run
- Run the `consumer.py` and the `producer.py` in seperate terminals to see the producer and the consumer outputs.

## Kafka Topics
- The docker-compose come with the environment variable: `KAFKA_CREATE_TOPICS` it create a topic automaticaly within the creation of the container. If you desire to use another topic just change the name, like `KAFKA_CREATE_TOPICS: "messages:1:1"` from **messages** to **events** `KAFKA_CREATE_TOPICS: "events:1:1"`. See [Automatically create topics](https://hub.docker.com/r/wurstmeister/kafka), from the Kafka image on Docker Hub.

### Any hassle make sure to watch the YouTube series from [better data science](https://www.youtube.com/watch?v=4xFZ_iTZLTs&list=PLQ5j-FTc2VhAY_PBg7FVkZsal50MCgp7Y). 