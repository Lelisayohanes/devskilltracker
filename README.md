devskilltracker/
│
├── apps/                              # All microservices & frontend
│   ├── auth-service/
│   ├── user-profile/
│   ├── job-board/
│   ├── submission/
│   ├── skill-tracker/
│   ├── rating-service/
│   ├── notification/
│   ├── api-gateway/
│   └── frontend/                      # Next.js app
│
├── charts/                            # Helm charts per service
│   ├── auth-service/
│   ├── user-profile/
│   ├── job-board/
│   └── ...                            # Other services
│
├── infra/                             # Infrastructure as Code
│   ├── terraform/                     # Terraform modules & envs
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   │   ├── provider.tf
│   │   ├── modules/
│   │   │   ├── cluster/               # K3d or Kind setup
│   │   │   ├── ingress/               # NGINX ingress
│   │   │   ├── monitoring/            # Prometheus, Grafana
│   │   │   └── jenkins/               # Optional: Jenkins Infra
│   │   └── environments/
│   │       ├── local/
│   │       └── staging/
│   ├── k3d/                           # K3d config files (optional)
│   ├── ingress/                       # Raw ingress YAML (if needed)
│   ├── monitoring/                    # Prometheus, Grafana, Loki
│   ├── jenkins/                       # Jenkins setup configs
│   └── nexus/                         # Nexus repo config
│
├── deployments/                       # Dev & CI deployment configs
│   ├── dev/
│   │   └── docker-compose.yml
│   └── ci/
│       └── docker-compose-ci.yml
│
├── .github/                           # GitHub Actions workflows
│   └── workflows/
│       ├── build.yml
│       ├── test.yml
│       ├── deploy.yml
│       └── trivy-scan.yml
│
├── scripts/                           # CLI & automation scripts
│   ├── build-images.sh
│   ├── setup-env.sh
│   ├── setup-k3d.sh
│   ├── deploy-local.sh
│   └── deploy-infra.sh
│
├── shared/                            # Shared libs and contracts
│   ├── proto/                         # gRPC protobuf definitions
│   └── utils/                         # Common utilities
│
├── .env                               # Root env vars
├── Makefile                           # Build/test/deploy commands
└── README.md
