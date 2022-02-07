# Advanced-dictionary
speaking dictionary values with python

import pyttsx3 #Please install the module pyttsx3 for speak
import datetime


engine = pyttsx3.init('sapi5')
voices = engine.getProperty('voices')

engine.setProperty('voice',voices[0].id)


def speak(audio):
    engine.say(audio)
    engine.runAndWait()



def wishMe():
    hour=int(datetime.datetime.now().hour)
    if hour>=0 and hour<12:
        print("😃😁")
        speak("Good morning sir. please search in the dictionary")
            
    elif hour>=12 and hour<18:
        print("😎")
        speak("Good afternoon. please search in the dictionary")
        
    else:
        print("🌃🌉")
        speak("Good evening. please search in the dictionary ")
if __name__ == "__main__":
    
    wishMe()




d1={"abbreviated":"Short,ened, or, contracted, so, that, a, part, stands, for,  the, whole",
"abberviation":"A shortened form of aword of phrase,standing for the whole","ability":"One of the sementic categories used in classification of modal verbs",
"ablative":"in older grammer a case that expresses meanings such as by N","absolute":"Plain grade or positive, used for possesive pronouns that can stand on their own (mine,yours,his,ours,theirs)",
"absolute clause":"A non finite or verbless clause containing its own subject","abstract":"Used mainly of nouns that denot an action,idea,quality or state",
"acceptability":"Of a language form or an utterence:the quality of being judged by native speakers as normal or possible","accidence":"The part of grammar that deals with the inflections of words change to indicate"





}



a=input("Search: ")

    
    
    
de=d1.keys()

if a not in de:
    
    print("Not in the dictionary")
    
    speak("Not in the dictionary")
    
else:
    print(d1.get(a))
    
    speak(d1.get(a))

