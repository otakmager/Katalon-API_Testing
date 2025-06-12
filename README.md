# 📊 Katalon-API\_Testing

This project implements **automated API testing** using **Katalon Studio 10.2.0**, targeting the [`https://reqres.in/`](https://reqres.in/) API. It includes **data-driven**, **negative**, **smoke**, and **regression** test suites covering key API endpoints related to user authentication and user management.

> ✅ Target URL: [https://reqres.in/](https://reqres.in/)
> 📦 GitHub Repo: [https://github.com/otakmager/Katalon-API\_Testing](https://github.com/otakmager/Katalon-API_Testing)

---

## 🧱 Project Structure

```
Katalon-API_Testing/
├── Data Files/
│   └── TD_CreateUser.dat
├── docs/
│   ├── TS_DataDriven_CreateUser.pdf
│   ├── TS_NegativeTest.pdf
│   ├── TS_RegressionTest.pdf
│   └── TS_SmokeTest.pdf
├── Object Repository/
│   └── API/
│       ├── Auth/
│       │   ├── POST_Login.rs
│       │   └── POST_Register.rs
│       └── User/
│           ├── DELETE_DeleteUser.rs
│           ├── GET_ListUsers.rs
│           ├── GET_SingleUser.rs
│           ├── PATCH_UpdateUser.rs
│           ├── POST_CreateUser.rs
│           └── PUT_UpdateUser.rs
├── Profiles/
│   └── default.glbl
├── Resources/
│   └── TestData.xlsx
├── Scripts/
├── settings/
├── Test Cases/
│   ├── Auth/
│   │   ├── Login/
│   │   └── Register/
│   └── User/
│       ├── DELETE/
│       ├── GET/
│       ├── PATCH/
│       ├── POST/
│       └── PUT/
└── Test Suites/
    ├── TS/
    └── TSC/
```

---

## ✅ Test Coverage

| Area        | Test Case Examples                               | Suite              |
| ----------- | ------------------------------------------------ | ------------------ |
| Auth        | Login success, missing email, missing password   | TS\_NegativeTest   |
| Register    | Register success, missing email/password         | TS\_NegativeTest   |
| User GET    | Get list, get single, not found                  | TS\_SmokeTest      |
| User POST   | Create user with data-driven inputs (Excel/.dat) | TS\_DataDriven     |
| User PUT    | Update full user info                            | TS\_RegressionTest |
| User PATCH  | Partial update                                   | TS\_RegressionTest |
| User DELETE | Delete user by ID                                | TS\_RegressionTest |

---

## 📄 Sample Reports

You can preview test results in PDF format (exported from Katalon Studio):

| Report Name                | Link                                                                                                     |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
| TS\_DataDriven\_CreateUser | [View PDF](https://github.com/otakmager/Katalon-API_Testing/blob/main/docs/TS_DataDriven_CreateUser.pdf) |
| TS\_NegativeTest           | [View PDF](https://github.com/otakmager/Katalon-API_Testing/blob/main/docs/TS_NegativeTest.pdf)          |
| TS\_RegressionTest         | [View PDF](https://github.com/otakmager/Katalon-API_Testing/blob/main/docs/TS_RegressionTest.pdf)        |
| TS\_SmokeTest              | [View PDF](https://github.com/otakmager/Katalon-API_Testing/blob/main/docs/TS_SmokeTest.pdf)             |

> 📝 *You can update or download these reports by re-running the corresponding Test Suite in Katalon.*

---

## 🚀 How to Run the Tests

### 1. Clone the Repository

```bash
git clone https://github.com/otakmager/Katalon-API_Testing.git
```

### 2. Open in Katalon Studio

* Open the project directory via `File → Open Project`

### 3. Run Test Suites

* Go to **Test Explorer > Test Suites > TS/**
* Right-click the desired suite (e.g. `TS_SmokeTest`) → **Run**

### 4. View Reports

* Reports will be available under the **Reports** section

---

## 📊 Data-Driven Testing

The `TS_DataDriven_CreateUser` suite demonstrates use of external test data.

| File                | Usage                                   |
| ------------------- | --------------------------------------- |
| `TD_CreateUser.dat` | Used as input dataset for `POST /users` |
| `TestData.xlsx`     | Alternative Excel-based source          |

Each row in the dataset represents a user payload submitted to the API.

---

## 🔧 Technologies Used

* Katalon Studio 10.2.0
* Groovy scripting
* Reqres API ([https://reqres.in/](https://reqres.in/))

---
