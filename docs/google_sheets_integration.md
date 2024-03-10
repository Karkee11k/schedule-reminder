# Google Sheets Integration

The Google Sheets Integration allows the project to retrieve the class
schedules from a Google Sheets. Follow these steps to set up and configure
the Google Sheets Integration.

1. **Obtain Google Sheets API Key:**
    - Go the the [Google Cloud Console](https://console.cloud.google.com/).
    - Create a new project or select an existing one.
    - Enable the Google Sheets API for your project.
    - Create credentials for the API and copy the API key.

2. **Set up Google Sheets Document:**
    - Create a google sheet that contains four inner sheets.
    - First Sheet format: 
        - Rename it 'calendar or any name you like'
        - Column A: Date (DD/MM/YYYY)
        - Column B: isWorkingDay (yes/no)
        - Column C: Day Order (1, 2, 3, ...)
    - Second Sheet format:
        - Rename it 'periods or any name you like'
        - Column A: First period
        - Column B: second period
        - ...
        - Column N: Nth period
    - Third Sheet format:
        - Rename it 'staffs or any name you like'
        - Column A: Staff for the first period
        - Column B: Staff for the second period
        - ...
        - Column N: Staff for the Nth period
    - Fourth Sheet format:
        - Rename it 'mail id or any name you like'
        - Column A: student1@gmail.com
        - Column B: Student name 
    - Make sure that the sheet is viewed by public.

3. **Configure Environment Variables:**
    - Add the Sheets ID to the '.env' file
    
4. Modify the sheets name in 'main.py'.

By setting up the Google Sheet Integration, the project can fetch data
from Google Sheets.