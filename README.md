# Observability Stack

통합 로그 및 메트릭 모니터링 스택 (ELK + Prometheus + Grafana)

## 🔧 구성 요소

### 로그 수집 및 분석 (ELK Stack)

- Filebeat: 컨테이너 로그 수집
- Elasticsearch: 로그 저장 및 검색
- Logstash: 로그 수집 및 파싱
- Kibana: 로그 시각화

### 메트릭 모니터링

- Prometheus: 메트릭 수집 및 저장
- Grafana: 통합 대시보드

## 🚀 실행

```bash
# 실행
docker-compose up -d

# 로그 확인
docker-compose logs -f
```

## 📁 디렉터리 구조

```
observability-stack/
├── docker-compose.yml
├── .env
├── elk/
│   ├── elasticsearch/
│   │   └── elasticsearch.yml
│   └── logstash/
│       └── logstash.conf
├── filebeat/
│   └── filebeat.yml
├── prometheus/
│   ├── prometheus.yml
│   └── alert.rules.yml
└── grafana/
    └── provisioning/
        └── datasources/
            └── datasources.yml
```

## ⚙️ 환경 변수 예시 (.env)

```
SECURITY_ENABLED=true # 개발: false, 운영: true
GRAFANA_ADMIN_USER=admin
GRAFANA_ADMIN_PASSWORD=admin123
```
