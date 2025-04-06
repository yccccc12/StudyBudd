# Project: StudyBudd
## Team Name: Error 403
## Members:
- GOH YI CHENG
- KOH SIN YEE
- LOW LIK HOW
- WONG JEA SEN

# Project Setup Instructions

## 🛠️ Prerequisites

Before running the project, ensure you have the necessary environment variables and API keys set up. Follow the steps below to configure your local environment.

### Required Keys and Files:

- **Gemini API Key**
- **Google Calendar ID**
- **Google Service Account JSON File**
- **Google Maps API Key**

## Set Up API Keys and Credentials

### 1. **Gemini API Key**
- Visit the [Gemini API website](https://www.gemini.com/) and log in or create an account.
- Navigate to the "API" section in your Gemini account.
- Generate a new API key and copy it for later use.

### 2. **Google Calendar ID**
- Open [Google Calendar](https://calendar.google.com).
- Select the calendar you want to use, click the three dots next to it, and choose "Settings and sharing."
- Under "Integrate calendar," locate and copy the **Calendar ID**.

### 3. **Google Service Account JSON File**
- Access the [Google Cloud Console](https://console.cloud.google.com/).
- Create a new project or select an existing one.
- Go to **IAM & Admin > Service Accounts**.
- Create a service account with the necessary permissions for the APIs (e.g., Google Calendar, Google Maps).
- Download the service account key in **JSON format** and store it securely.

### 4. **Google Maps API Key**
- Open the [Google Cloud Console](https://console.cloud.google.com/).
- Navigate to **APIs & Services > Credentials**.
- Generate a new API key under **Create credentials**.
- Enable the **Maps JavaScript API** and any other APIs required for your project.

## 5. Grant Google Service Account Access to Calendar
- Open [Google Calendar](https://calendar.google.com/).
- Click the **three dots** next to your calendar and select **Settings and sharing**.
- Scroll down to **Share with specific people** and click **Add people**.
- Enter your **Google Service Account email** (e.g., `your-service-account@your-project-id.iam.gserviceaccount.com`).
- Choose **Make changes to events** or appropriate permissions.
- Click **Send** or **Add** to grant access.

## 6. Enable Google Calendar API and Gemini API
1. In the **Google Cloud Console**, go to **APIs & Services > Library**.
2. Search for **Google Calendar API** and enable it for your project.
3. Repeat Step 2 for **Google Maps API** to ensure all required APIs are active.
4. Verify that the APIs are enabled by navigating to **APIs & Services > Enabled APIs & Services** in the Google Cloud Console.

## Set Up and Run the Project

### 1. **Clone the Repository**
Clone the project repository from GitHub:

```bash
git clone https://github.com/yccccc12/StudyBudd.git
```

### 2. **Install Required Packages**
Install the dependencies listed in the `requirements.txt` file:

 ```bash
 pip install -r requirements.txt
 ```

### 3. **Add Credentials to the Project**
1. Place the downloaded **Google Service Account JSON file** in the root directory of the project.
2. Rename the file to `google_credentials.json`.
3. Find a file named `credentials.json` in the root directory and paste the following structure into it:

```json
{
    "gemini_api_key": "YOUR_GEMINI_API_KEY",
    "calendar_id": "YOUR_GOOGLE_CALENDAR_ID",
    "google_map_api_key": "YOUR_GOOGLE_MAPS_API_KEY"
}
```

4. Replace `YOUR_GEMINI_API_KEY`, `YOUR_GOOGLE_CALENDAR_ID`, and `YOUR_GOOGLE_MAPS_API_KEY` with the actual values you obtained earlier.
5. Save the file securely.

### 4. **Navigate to the Project Directory**
Open a terminal and navigate to the directory where the project is located.

### 5. **Run the Application**
Start the application using Streamlit:

```bash
streamlit run app.py
```
