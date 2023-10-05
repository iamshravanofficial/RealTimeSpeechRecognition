# Real Time Speech Recognition

Brief description of the project.

## About

code serves as a real-time speech recognition and translation tool, enabling users to speak in one language and hear their words translated into another language of their choice, all within the Python environment.

## Getting Started

The code begins by importing several Python libraries, including playsound, speech_recognition, googletrans, gtts (Google Text-to-Speech), and os.
Language Dictionary: The code defines a tuple named dic, which contains pairs of languages and their corresponding codes. This dictionary maps user input to language codes later in the script.
takecommand() Function: This function captures voice input from the user through the microphone using the speech_recognition library.
It listens for user input, recognizes the speech, and returns the recognized text as a string.
If speech recognition fails, it returns "None."
User Input: The script captures the user's voice input and stores it in the query variable. It repeatedly prompts the user if speech recognition fails or returns "None."
destination_language() Function: This function prompts the user to specify the language they want to translate the input into.
It returns the language name (e.g., "Hindi") as a lowercase string.
Mapping to Language Code: The script maps the user's specified destination language to its corresponding language code using the dic dictionary.
Translation: It uses the Google Translate API from the googletrans library to translate the user's input (stored in query) into the destination language specified.
The translated text is stored in the text_to_translate variable.
Text-to-Speech: The translated text is converted into speech in the destination language using the Google Text-to-Speech (gTTS) library (gtts).
The generated speech is saved as an MP3 file named "captured_voice.mp3."
Playback and Cleanup: The code plays the translated speech using the playsound library.
After playing the speech, it removes the "captured_voice.mp3" file to clean up the workspace.
Printing Output: Finally, the code prints the translated text to the console.
