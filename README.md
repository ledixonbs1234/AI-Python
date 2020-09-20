import speech_recognition

bot_brain = ""
bot_ear= speech_recognition.Recognizer()
with speech_recognition.Microphone() as mic:
    print("\nSiri: I'am Listening:..")
    audio = bot_ear.record(mic,3)
    print("\nSiri:..")
try:
    you = bot_ear.recognize_google(audio,language='vi-VN')
    
    if "mo ti vi" in you:
        bot_brain = "Ban da mo ti vi"
        print(bot_brain)
        
    print("\nYou: "+you)
except:
    you ="Toi khong hieu ban noi gi"
    print("\nSiri: "+you)
