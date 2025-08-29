---
sidebar_position: 2
---

##### Role
- Created an IoT microservice using Golang http/server modules
- Microservice has Kafka as a backend
- Created Kafka consumers to process/write data into timeseries DB
- Achieved write throughput of 10K msgs/sec to kafka
- Created middlewares for rate limiting
- Used uber/zap logger for fast logging
- Integrated open-telemetry solutions
- Traces and API metrics were pushed to live reporting system(Jaeger and Grafana)
- TimeSeries data was aggregated for various intervals
- To fetch Timeseries data API was created

##### Performance Metrics 
- PUT TimeSeries latency within 200 ms for 10K writes/sec
- GET TimeSeries latency within 800 ms for 2K reads/sec

##### Challenges faced and fixed
- Hot partition in Kafka
- Poor scaling of consumers

##### Lessons Learnt
- Distribute messages on Kafka using "Custom keys"
- For high rate messages create different topics - avoids noisy neighbours
- Implement Retry and DLQ topics

##### Achievements
- Service is cloud agnostic
- Cloud cost was optimized