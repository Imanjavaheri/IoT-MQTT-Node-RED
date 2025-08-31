# IoT-MQTT-Node-RED
This project implements an IoT data pipeline using MQTT, Node-RED, CSV logging, and ThingSpeak integration. It generates random IDs and timestamps, processes messages through multiple flows, filters publish events, logs acknowledgements, and visualizes temperature data.

Main Tasks:

1. ID & Timestamp Generation – Create random IDs every 5s, publish to MQTT (challenge3/id_generator), and log into challenge3.csv.

2. CSV Lookup – On subscription, compute ID % 7711 and retrieve matching row from CSV.

3. Publish Handling – Forward messages if type = Publish Message, add timestamp & topic, rate-limited to 4/min.

4. Temperature Data – Extract °F values, compute mean, plot chart, and save to filtered_pubs.csv.

5. ACK Logging & Cloud Upload – Count ACKs, save to ack_log.csv, and update ThingSpeak channel (ID: 2930856).
