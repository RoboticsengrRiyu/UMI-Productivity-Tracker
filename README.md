# UMI Data Collection Platform
### Real-Time Operator Productivity & Quality Web Application

https://img.shields.io/badge/React-18-blue.svg\]()
https://img.shields.io/badge/FastAPI-Latest-green.svg\]()
https://img.shields.io/badge/Firebase-Cloud-orange.svg\]()
https://img.shields.io/badge/PostgreSQL-Database-blue.svg\]()

A cloud-based web application designed for NVIDIA UMI Data Collection operations to monitor operator productivity, data quality, attendance, task completion, and dataset acceptance in real time.

---

# Features

## Operator Dashboard

Monitor individual operator performance.

### Metrics

- Datasets Collected
- Demonstrations Completed
- Collection Time
- Active Time
- Idle Time
- Upload Success Rate
- Quality Score
- Acceptance Rate
- Productivity Score

---

## Team Lead Dashboard

Monitor the entire data collection team.

### Team KPIs

- Total Datasets Collected
- Active Operators
- Average Productivity
- Average Quality
- Team Acceptance Rate
- Operator Ranking
- Shift Coverage
- Team Utilization

---

## Quality Dashboard

Track quality-related issues.

### Quality Metrics

- Dataset Rejections
- Missing Metadata
- Annotation Errors
- Camera Calibration Errors
- Rework Requests
- Defect Trends

---

## Real-Time Monitoring

### Live Updates

```text
✅ Operator Status
✅ Dataset Collection Activity
✅ Upload Progress
✅ Dataset Validation
✅ Quality Inspection
✅ Team Dashboard Refresh
```

---

# Technology Stack

## Frontend

```text
React.js
Tailwind CSS
Material UI
Recharts
Axios
React Router
```

---

## Backend

```text
FastAPI
Python
JWT Authentication
WebSockets
Background Services
```

---

## Database

```text
PostgreSQL
Firebase Firestore
Redis Cache
```

---

## Cloud Hosting

### Google Cloud

```text
Cloud Run
Cloud SQL
Firebase Hosting
Firestore
Cloud Storage
```

Works directly in:

```text
✅ Google Chrome
✅ Microsoft Edge
✅ Firefox
✅ Safari
✅ Android
✅ iPhone
✅ Tablet
```

---

# Operator Workflow

```text
Login
   │
   ▼
Start Collection Session
   │
   ▼
Record UMI Demonstration
   │
   ▼
Upload Dataset
   │
   ▼
Automatic Quality Validation
   │
   ▼
Project Review
   │
   ▼
Dataset Accepted
```

---

# Productivity Formula

## Productivity Score

```text
Productivity Score =
(Completed Tasks ÷ Assigned Tasks) × 100
```

### Example

```text
Completed Tasks = 95
Assigned Tasks = 100

Productivity = 95%
```

---

# Quality Formula

## Quality Score

```text
Quality Score =
100 - (
Capture Errors +
Metadata Errors +
Annotation Errors
)
```

### Example

```text
Quality Score = 98%
```

---

# Operator Performance Formula

```text
Overall Score =
40% Productivity +
40% Quality +
20% Attendance
```

---

# Dashboard Pages

## Home Dashboard

```text
Datasets Today
Productivity Score
Quality Score
Acceptance Rate
```

---

## Operators

```text
Operator List
Current Shift
Status
Performance
```

---

## Team Analytics

```text
Weekly Productivity
Monthly Productivity
Trend Analysis
Leaderboard
```

---

## Quality Analytics

```text
Defect Analysis
Rework Trends
Acceptance Trends
Validation Reports
```

---

# Database Schema

## Operators

```sql
CREATE TABLE operators (
    id SERIAL PRIMARY KEY,
    employee_id VARCHAR(50),
    name VARCHAR(100),
    shift VARCHAR(50),
    status VARCHAR(20),
    productivity_score DECIMAL(5,2),
    quality_score DECIMAL(5,2),
    attendance_score DECIMAL(5,2)
);
```

---

## Datasets

```sql
CREATE TABLE datasets (
    id SERIAL PRIMARY KEY,
    operator_id INTEGER,
    dataset_name VARCHAR(255),
    collected_at TIMESTAMP,
    accepted BOOLEAN,
    quality_score DECIMAL(5,2),
    upload_status VARCHAR(20)
);
```

---

# API Endpoints

## Operators

```http
GET /api/operators

GET /api/operators/{id}

POST /api/operators
```

---

## Productivity

```http
GET /api/productivity

POST /api/productivity/update
```

---

## Quality

```http
GET /api/quality

POST /api/quality/report
```

---

## Dashboard

```http
GET /api/dashboard

GET /api/dashboard/live
```

---

# User Roles

## Operator

Permissions:

```text
View Personal Dashboard
Start Collection Session
Upload Dataset
View Quality Results
```

---

## Quality Analyst

Permissions:

```text
Review Datasets
Approve Datasets
Reject Datasets
Create Quality Reports
```

---

## Project Lead

Permissions:

```text
View Team Dashboard
Monitor Productivity
Track Quality
Generate Reports
Manage Operators
```

---

# KPI Targets

| KPI | Target |
|-------|----------|
| Productivity Score | > 90% |
| Quality Score | > 95% |
| Acceptance Rate | > 95% |
| Upload Success | 100% |
| Attendance | > 98% |
| Rework Rate | < 2% |

---

# Future Enhancements

### NVIDIA UMI Integration

```text
✅ Dataset Validation Engine
✅ OAK-D Camera Monitoring
✅ Robot Station Utilization
✅ Real-Time Dataset Tracking
✅ Multi-Camera Synchronization
✅ AI Quality Inspection
✅ Defect Prediction
✅ Analytics Dashboard
✅ Team Leaderboard
✅ Power BI Export
✅ Excel Export
✅ Weekly Productivity Reports
✅ Monthly Quality Reports
✅ Shift Scheduling
✅ Attendance Tracking
```

---

# Deployment

## Frontend

```bash
npm install
npm run build
```

---

## Backend

```bash
pip install -r requirements.txt

uvicorn main:app --reload
```

---

## Firebase Deployment

```bash
npm install -g firebase-tools

firebase login

firebase init

firebase deploy
```

---

# Repository Structure

```text
umi-data-collection-platform/
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   └── dashboard/
│
├── backend/
│   ├── api/
│   ├── quality/
│   ├── productivity/
│   ├── analytics/
│   └── reports/
│
├── database/
│
├── docs/
│
├── tests/
│
├── docker/
│
└── README.md
```

---

# Repository Name

```text
umi-data-collection-platform
```

### Description

```text
Enterprise-grade real-time web application for NVIDIA UMI Data Collection operations, providing operator productivity tracking, quality monitoring, dataset validation, analytics, reporting, and project management dashboards accessible through Google Chrome and cloud-hosted infrastructure.
```
