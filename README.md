
---

# Microfrontend Task Tracker

A hybrid **Microfrontend** application built with **Angular** and **React**, connected using **Webpack Module Federation**.

The app allows users to manage tasks, filter by status, and view basic dashboard statistics using a mock backend.

---

## Architecture Overview

| App         | Framework   | Port | Purpose                       |
| ----------- | ----------- | ---- | ----------------------------- |
| Shell       | Angular     | 4200 | Main host application         |
| List Remote | Angular     | 4201 | Sidebar, dashboard, task list |
| Edit Remote | React       | 4202 | Create & edit task modal      |
| Mock Server | JSON Server | 3000 | REST API backend              |

---

## Prerequisites

* Node.js installed

---

## Installation

Run this in **each project folder**:

```bash
npm install
```

Folders:

* `shell`
* `list-remote`
* `edit-remote`
* `mock-server`

---

## Running the Application

You need **4 terminals**.

### 1. Mock Backend

```bash
cd mock-server
npx json-server --watch db.json --port 3000
```

API: [http://localhost:3000/todos](http://localhost:3000/todos)

---

### 2. List Remote (Angular)

```bash
cd list-remote
npm start
```

Runs on [http://localhost:4201](http://localhost:4201)

---

### 3. Edit Remote (React)

```bash
cd edit-remote
npm start
```

Runs on [http://localhost:4202](http://localhost:4202)

---

### 4. Shell (Host App)

```bash
cd shell
npm start
```

Open: [http://localhost:4200](http://localhost:4200)

---

## Features

* Angular Shell loading React components
* Create, update, delete tasks
* Dashboard task statistics
* Filter tasks (All / Pending / Done)
* Dark mode UI

---

## Tech Stack

* Angular 19
* React 18
* Webpack 5 (Module Federation)
* JSON Server
* RxJS & React Hooks

---
