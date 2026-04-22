# Human-Rights-Monitor-Web-Services-Project


A modern case management platform for documenting, analyzing, and monitoring human rights violations in the field. Built using FastAPI, MongoDB, and Streamlit.



---



## 1️⃣ Overview



The Human Rights MIS system enables NGOs and legal teams to:



- Record human rights cases (e.g., arbitrary detention, forced displacement)

- Manage victims and witness data securely

- Submit incident reports with geolocation and media attachments

- Analyze trends via visual analytics and exportable reports



---



## 2️⃣ Key Features



### 🧾 Case Management

- ✅ Create, view, update, and archive cases

- 🔄 View full case status history



### 📎 Evidence Handling

- 📁 Upload and attach PDFs, images, and videos to specific cases



### 📊 Analytics & Reporting

- 🥧 Pie chart of violations

- 📊 Bar chart by country

- 📈 Timeline chart by month

- 📥 Export filtered data to Excel



### 🔍 Smart Filtering

- Filter cases by:

  - Country

  - Violation type

  - Case status

  - Date range



### 🌐 Clean UI & Navigation

- Streamlit-based modular UI

- Sidebar and dashboard navigation

- Inline alerts and success messages



---



## 3️⃣ Technologies Used



- 🐍 Python 3.12

- 🚀 FastAPI + Uvicorn (Backend API)

- 🍃 MongoDB (NoSQL Database)

- 🧾 Pydantic (Validation Models)

- 📊 Streamlit (Frontend)

- 📦 Libraries:

  - Plotly (Charts)

  - Requests (API calls)

  - Pandas, OpenPyXL (Excel export)



---



## 4️⃣ Folder Structure



```

.

├── app.py                     # Streamlit UI entry point

├── main.py                    # FastAPI backend entry point

├── populate_cases.py          # Script to insert sample/test data

├── final_project.pdf          # Project documentation (PDF)

├── README.md

├── requirements.txt

├── .gitignore

├── database/                  # MongoDB connection setup

├── models/                    # Pydantic models (for FastAPI and potentially shared with Streamlit)

├── routers/                   # API route definitions (FastAPI endpoints)

├── frontend/                     # Streamlit pages (UI modules)

├── uploads/                   # Uploaded evidence files (should be excluded from Git)

├── documentation/             # NEW: Folder for API documentation artifacts for Incident Reporting Module 

│   ├── openapi.json          

├── postman/

│   └── Human Rights MIS API.postman_collection.json # API testing collection

```





## 5️⃣ How to Run the Project



### ▶️ 1. Backend (FastAPI)

```bash

uvicorn main:app --reload

```



### ▶️ 2. Frontend (Streamlit Dashboard)

```bash

streamlit run app.py

```



### ▶️ 3. Load Sample Data (Optional)

```bash

python populate_cases.py

```



### ▶️ 4. Install Dependencies

```bash

pip install -r requirements.txt

```



---



## 6️⃣ API Documentation



### 🧾 Case Endpoints

- `POST /cases/` – Create new case

- `GET /cases/` – List all cases (with optional filters)

- `GET /cases/{case_id}` – Retrieve a specific case

- `PATCH /cases/{case_id}` – Update all case fields

- `PATCH /cases/{case_id}/status` – Update case status only

- `DELETE /cases/{case_id}` – Archive a case

- `GET /cases/{case_id}/history` – View case status history

- `POST /cases/{case_id}/upload` – Upload a file to a case





### 🧾 Incident Reporting Endpoints

- `POST /reports/` – Submit a new incident report

- `GET /reports/` – List reports (filter by status, date, location)

- `PATCH /reports/{report_id}` – Update report status

- `GET /reports/analytics` – Count reports by violation type

-  `GET /reports/{report_id}` – Retrieve a single incident report by its unique ID, to view specific report details.





### 📊 Analytics Endpoints

- `GET /analytics/violations` – Violation summary (supports filters)

- `GET /analytics/geodata` – Distribution by country

- `GET /analytics/timeline` – Monthly timeline of cases



---



## 📘 API Documentation Access

Swagger UI: http://127.0.0.1:8000/docs



ReDoc: http://127.0.0.1:8000/redoc



---



## 8️⃣ Contributors



| Name               | Role                                      |

|--------------------|-------------------------------------------|

| **Munawwar Qamar** | Case Management, Dashboard, Analytics     |

| **Ayah**            | Victim & Witness Module                   |

| **Shahd**          | Incident Reporting & Validation Modules   |



---



## 9️⃣ Acknowledgements



- [`Streamlit Option Menu`](https://github.com/victoryhb/streamlit-option-menu) – For custom navigation

- [`MongoDB Aggregation Framework`](https://www.mongodb.com/docs/manual/aggregation/) – For filtering & statistics

- [`FastAPI`](https://fastapi.tiangolo.com/) – API framework

- [`Plotly Express`](https://plotly.com/python/plotly-express/) – Visual analytics

- [`OpenPyXL`](https://openpyxl.readthedocs.io/) – Excel exporting



---



✅ _Project developed as part of a university course on Web Services._

