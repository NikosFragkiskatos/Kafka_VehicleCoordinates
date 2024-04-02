# Confluent Kafka Demo - Vehicle Coordinates

This project demonstrates a real-world application of Apache Kafka for handling streaming IoT data at scale. It constructs a web server using Kafka, employing Docker for creating a Kafka cluster, Python for publishing vehicle location data, and Node.js for consuming the published data. This demo provides a solid foundation for understanding how to work with Kafka in a microservices architecture. The Word file "Screenshots of Project Execution" is my submission to the project on Kafka for MIT.

## Installation
### Prerequisites
- Docker Desktop with at least 6 GB of memory allocated
- Python 3.x
- Node.js 12.x or newer
- Microsoft Visual Studio (for Windows)

## Setup

### 1. Use a terminal and cd into a known directory. Then clone the repository using the following command:

`git clone https://github.com/NikosFragkiskatos/Kafka_VehicleCoordinates.git`

### 2. Configure Docker Desktop
- Open Docker Desktop settings.
- Allocate at least 6 GB of memory under the Resources tab.

### 3. Windows Users:
- Inside your user home folder (`C:\Users\YOUR_WINDOWS_USERNAME`), create a .wslconfig file with the following configuration:
- Allocate at least 6 GB of memory under the Resources tab.
  
`[wsl2]`
`memory=8GB # Limits VM memory in WSL 2`  
`processors=4 # Makes the WSL 2 VM use 4 virtual processors`  
`localhostForwarding=true # Enables localhost forwarding`

### 4. Initialize Kafka Container:
- Navigate to the kafka-docker folder and run:
docker-compose up
Verify that the Kafka container components are up and running in Docker Desktop.

## Dependencies

Install the required Python and Node.js dependencies:  
### Windows Users:

- In a Terminal window, run the commands below to install the Express and node-rdkafka libraries:  
`npm install express`
`npm install node-rdkafka`

### Mac Users:

- In a Terminal window, run the commands below to install the Express and node-rdkafka libraries:
`sudo xcode-select --reset`
`npm install express`
`npm install node-rdkafka`

## Usage

### 1. Start the Kafka Producer:
- Open the `PublishVehicleCoordinates.py` file in the pythonProducer folder and run:
python PublishVehicleCoordinates.py
### 2. Start the Node.js Web Server:
- In the `NodeJSConsumer` folder, run:
node server.js
### 3. Access the Web Interface:

- Open a browser and navigate to http://localhost:5000 to see the web interface.

### 4. Consume Vehicle Coordinates:

- Click on the "Consume Vehicle Coordinates" button to start consuming data from the Kafka topic.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/AmazingFeature)
3. Commit your Changes (git commit -m 'Add some AmazingFeature')
4. Push to the Branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the `LICENSE.txt` file for details.


