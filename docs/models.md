# 📦 Modelos de Datos

## User
- name: string
- email: string
- password: string (hash)

---

## Device
- userId: string
- dId: string
- name: string
- actuators: array
- locationId: string
- locationName: string

---

## Location
- name: string
- description: string
- devices: array

---

## Data
- locationName: string
- deviceName: string
- deviceId: string
- habitacion: string
- valor: number
- createdTime: number
