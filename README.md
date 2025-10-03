# voice-assistant-Ai
# voice-assistant-Ai
🤖 Vishal Assistant (Voice Activated Desktop Assistant)
This is a personal desktop assistant built in Python. It uses Speech Recognition to understand voice commands and Text-to-Speech to provide audible responses, automating various common desktop tasks like browsing, getting information, and managing files.

✨ Features
The Vishal Assistant can perform the following voice-activated tasks:

Command Phrase	Action Performed	Libraries Used
"wikipedia [topic]"	Searches and reads a 2-sentence summary of the topic from Wikipedia.	wikipedia
"open youtube"	Opens YouTube in the default web browser.	webbrowser
"open google"	Opens Google in the default web browser.	webbrowser
"open stackoverflow"	Opens Stack Overflow in the default web browser.	webbrowser
"play music"	Plays the first song from a specified local directory (D:\Non Critical\songs\Favorite Songs2).	os
"the time"	Announces the current system time.	datetime
"open code"	Launches a specified executable (e.g., VS Code) from a hardcoded path.	os
"email to vishal"	Prompts the user for email content and attempts to send it to a specified recipient. (Requires setup)	smtplib

Export to Sheets
🛠️ Prerequisites and Setup
To run this assistant, you need to have Python installed along with the following libraries:

1. Installation
You can install all necessary Python packages using pip:

Bash

pip install pyttsx3 SpeechRecognition wikipedia
2. Configuration
A. Text-to-Speech:

The script uses pyttsx3 and is configured to use the SAPI5 voice engine (voices[0].id), which is common on Windows systems.

B. Speech Recognition:

The takeCommand() function uses the Google Speech Recognition API (requires an active internet connection).

C. Email Functionality (Crucial Security Note):

The sendEmail() function uses smtplib for sending mail via Gmail.

You must update the following placeholders in the sendEmail function:

'youremail@gmail.com'

'your-password' (or an App Password for enhanced security, as Google often blocks direct password login)

Highly Recommended: Use a Google App Password instead of your main account password, as using your plain password can be a security risk.

D. Hardcoded Paths:

For play music and open code commands, you must update the file paths to match your local machine:

music_dir = 'D:\\Non Critical\\songs\\Favorite Songs2'

codePath = "C:\\Users\\Haris\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe"

▶️ How to Run the Assistant
Ensure all prerequisites are installed and configured.

Run the script from your terminal:

Bash

python your_script_name.py
The assistant will greet you: "I am vishal assistant. Please tell me how may I help you"

Wait for the "Listening..." prompt, then speak your command (e.g., "open youtube" or "tell me the time").

The assistant will execute the task and confirm with an audible response.

