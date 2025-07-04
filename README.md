# Notification-Dispatch-System

notification-system/
│
├── docker-compose/         # Kafka, Zookeeper, Kafka UI
│   ├── docker-compose.yml
│   └── .env
│
├── services/
│   ├── event-api/          # REST API -> Kafka producer
│   ├── notification-worker/# Kafka consumer -> email/SMS
│   └── audit-logger/       # Kafka consumer -> S3/DB
│
├── libs/                   # Shared Java libs (DTOs, utils, common config)
│   └── commons/
│
├── deploy/                 # AWS deploy configs (ECS task defs, scripts)
│   ├── ecs/
│   └── github-actions/
│
├── infra/                  # Terraform or CloudFormation (optional later)
│
├── README.md
└── .gitignore
