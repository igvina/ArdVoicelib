#ArdVoicelib: A library to play audio (voices) on the Arduboy
By @igvina
##Features:
###Voice library:
* Play compressed audio (works better with voices)
* Good speed but can cause slowdowns on 60 fps games 
* Configurable speed (from 0.8 to 1.3)

###Voice compressor:
* Works with wav (only 8000 Hz, mono, 1 byte PCM_UNSIGNED). I recommend Audacity to convert to this format.
* Configurable quality (from 0 to 10), default is 4
* Good compression (from 88 bytes/s to 530 bytes/s)

##Usage:
###Vocoder (v0.1):
* Syntax: java -jar vocoder.jar audio.wav [-options]
	* options:
		* -q VALUE		Quality (0 - 10) default: 4
		* -gs SKETCH_FOLDER	Generate sketch code
		* -v			Play compressed voice
		* -anp PREFIX		Array name prefix
		* -ver			Show vocoder version

	* examples:
	
        	"java -jar compressor.jar dog.wav -gs DOG -v -q 6"
        	"java -jar compressor.jar merry.wav -v"
	
###Voice library (0.1):

* Copy lib (ArdVoicelib.h and ArdVoicelib.cpp) to your project folder
* Add in .ino file:
	* \#include "ArdVoicelib.h"
	* ArdVoicelib ardvoice;
* To play voice call function: ardvoice.playVoice (...).

####Methods:
* void playVoice(const char *audio);
* void playVoice(const char *audio, uint16_t startTime, uint16_t endTime, float speed);
* void stopVoice();
* boolean isVoicePlaying();
	

