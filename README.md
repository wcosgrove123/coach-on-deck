Coach on Deck 🏊‍♂️
Coach on Deck is a modern, web-based application for designing and building swimming practices. It combines a powerful manual practice builder with "Coach," an AI assistant powered by a local large language model (LLM), to help you create effective and creative workouts in seconds.

Whether you're a seasoned coach planning for a whole team or an individual swimmer looking to structure your training, Coach on Deck provides the tools you need right on your local machine.

Core Features
Manual Practice Builder: Intuitively add, delete, and reorder sets and rows. Easily adjust repetitions, distances, and descriptions.

Automatic Calculations: The app instantly calculates the total yardage, total practice time, and pace-per-100 for every interval, taking the guesswork out of your workout design.

AI Assistant ("Coach"): Describe your training goal in plain English (e.g., "a 4000-yard aerobic freestyle practice"), and let Coach generate a complete, well-structured workout for you.

Local-First AI: All AI processing is handled locally on your machine via Ollama. Your data and prompts are never sent to the cloud, ensuring complete privacy.

Fully Self-Contained: The entire application runs from a single HTML file, requiring no complex installation or web server.

How to Get Started
Follow these steps to get Coach on Deck running on your local machine.

1. Prerequisites: Install Ollama
This application requires Ollama to be installed to power the AI features.

Go to the official Ollama website and download the installer for your operating system (Windows, macOS, or Linux).

Follow the installation instructions.

2. Download the AI Model
For the best results, "Coach" needs a capable instruction-tuned model. We recommend using llama3:8b-instruct.

Open your terminal (PowerShell, Command Prompt, or Terminal).

Run the following command to download the model:

ollama pull llama3:8b-instruct

3. Configure Ollama for the App (One-Time Setup)
To allow the app to communicate with Ollama, you need to configure a CORS setting. The easiest way is to set a permanent environment variable.

For Windows:

Search for "Edit the system environment variables" in the Start Menu and open it.

Click "Environment Variables...".

Under "System variables," click "New...".

Set Variable name: OLLAMA_ORIGINS

Set Variable value: *

Click OK on all windows to save.

Restart the Ollama application by quitting it from your system tray and starting it again.

For macOS/Linux:

You can set this in your shell profile (.zshrc, .bash_profile, etc.) by adding the line: export OLLAMA_ORIGINS='*'

4. Run the Application
Make sure the Ollama desktop application is running in the background.

Simply double-click the swim_app.html file to open it in your web browser.

You are now ready to start building practices!

Usage
Building a Practice Manually
Use the "+ Add New Set" button to create workout blocks.

Within each set, use the "Add Row" button to add individual lines.

Fill in the Reps, Dist, Interval, and Description for each line. The totals and pace will update automatically.

Adjust the "Repeat Set" value to multiply a set (e.g., for 3x through).

Using "Coach" (AI Assistant)
In the AI Coach Assistant box, type a clear description of the workout you want. Be as specific as you like!

Simple Example: a 3000 yard practice

Detailed Example: an hour-long practice for age-group swimmers focused on backstroke drills and kicking

Click the "Generate Practice" button.

The first generation may take a minute as the model loads into memory. Subsequent requests will be much faster.

Coach will generate a complete practice and populate the builder for you. You can then edit it as needed.

Future Development
The vision for Coach on Deck is to become an even smarter coaching partner. The next major step is to implement a Retrieval-Augmented Generation (RAG) system using a Supabase database. This will allow "Coach" to learn from a curated set of elite, real-world practices, dramatically improving the quality and relevance of its workout suggestions.
