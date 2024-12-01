# Student Data AWS Serverless Web App

## 📖 Übersicht
Dies ist eine serverlose Web-App, die in AWS implementiert wurde. Die App ermöglicht es, Daten von Studierenden in einer DynamoDB-Datenbank zu speichern und abzurufen. Sie nutzt mehrere AWS-Services, um eine skalierbare und kosteneffiziente Lösung bereitzustellen.

## 🔧 Technologien und AWS-Services
- **Frontend**:
- Statische Webseite gehostet mit AWS CloudFront.
- **Backend**:
  - **AWS Lambda**: Für die Verarbeitung von GET- und POST-Anfragen.
  - **Amazon API Gateway**: Schnittstelle zwischen Frontend und Backend.
  - **Amazon DynamoDB**: Serverlose NoSQL-Datenbank zur Speicherung der Studentendaten.
- **Hosting**:
  - CloudFront für die Bereitstellung des Frontends.

## 🚀 Funktionen
1. **Daten abrufen**: Eine GET-API ruft die Daten aus DynamoDB ab.
2. **Daten hinzufügen**: Eine POST-API fügt neue Daten zur Datenbank hinzu.
3. **Frontend**: Ein einfaches Interface zur Anzeige und Eingabe von Studentendaten.

## 🛠️ Projektstruktur
studentData-AWS-Serverless-Web-App/
├── frontend/             
│   ├── index.html
│   └── script.js
├── lambda-functions/     
│   ├── getStudent.js
│   └── insertStudentData.js
├── README.md            

## 📂 DynamoDB Datenstruktur
Die App verwendet eine DynamoDB-Tabelle, um die Daten der Studierenden zu speichern. Hier ist ein Beispiel für die Struktur:

| studentId | age | class | name          |
|-----------|-----|-------|---------------|
| 1         | 19  | A     | cedric        |
| 2         | 20  | B     | zweiterStudent|

### Tabelleinstellungen
- **Primärschlüssel**: `studentId` (String)
- **Attribute**:
  - `studentId`: Eindeutige ID für jeden Studierenden.
  - `age`: Alter des Studierenden.
  - `class`: Klasse oder Kurszuordnung.
  - `name`: Name des Studierenden.

## 📂 DynamoDB Datenstruktur
Die App verwendet eine DynamoDB-Tabelle, um die Daten der Studierenden zu speichern. Hier ist ein Beispiel für die Struktur:

| studentId | age | class | name          |
|-----------|-----|-------|---------------|
| 1         | 19  | A     | cedric        |
| 2         | 20  | B     | zweiterStudent|

### Tabelleinstellungen
- **Primärschlüssel**: `studentId` (String)
- **Attribute**:
  - `studentId`: Eindeutige ID für jeden Studierenden.
  - `age`: Alter des Studierenden.
  - `class`: Klasse oder Kurszuordnung.
  - `name`: Name des Studierenden.

### Beispiel-Daten (JSON)
Einträge in der Tabelle sehen wie folgt aus:
```json
{
  "studentId": "1",
  "age": 19,
  "class": "A",
  "name": "cedric"
},
{
  "studentId": "2",
  "age": 20,
  "class": "B",
  "name": "zweiterStudent"
}

