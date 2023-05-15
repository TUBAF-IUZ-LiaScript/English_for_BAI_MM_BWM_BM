[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/TUBAF-IUZ-LiaScript/English_for_BAI_MM_BWM_BM/main/arduino.md#1)

<!--

author: Toni Sand


import: https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md
        

-->

# Pie Demon bring Harm

!?[](https://www.youtube.com/watch?v=zmtYqTjcFYI)

## Simulation

<div id="matrix-experiment">
<wokwi-neopixel-matrix pin="6" cols="9" rows="9"></wokwi-neopixel-matrix>
<span id="simulation-time"></span>
</div>

```cpp             Automata
#include "FastLED.h"
#define DATA_PIN 6
#define BRIGHTNESS 254
#define NUM_LEDS 11
int i = 0;

CRGB leds[NUM_LEDS];

void setup() {
  FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
  FastLED.setBrightness(BRIGHTNESS);
}

int numbers[] = {3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 8, 9, 7, 9, 3, 2, 3, 8, 4, 6, 2, 6, 4, 3, 3, 8, 3, 2, 7, 9, 5, 0, 2, 8, 8, 4, 1, 9, 7, 1, 6, 9, 3, 9, 9, 3, 7, 5, 1, 0};

void loop() {
	
	for (int i = 0; i<NUM_LEDS; i++){
		if ((i)%2) {
			leds[i] = CRGB::Blue;
		}else{
		leds[i] = CRGB::Red;	
		}
	}
	FastLED.show();
	delay(2021);
	
	for (int j = 0; j < NUM_LEDS; j++)
        { 
         leds[j] = CRGB::Black;

        }
             FastLED.show();
	
	
	for (int i = 0; i<50; i++) {
		for (int j = 0; j<numbers[i]; j++) {
			leds[j] = CRGB::Green;
 
		}
					            FastLED.show();
		delay(3142);
		for (int j = 0; j < NUM_LEDS; j++)
        { 
         leds[j] = CRGB::Black;

        }
             FastLED.show();
	}

	for (int i = 0; i<500; i++){
	    for (int i = 0; i<NUM_LEDS; i++){
	    	leds[i] = CRGB::White;
	}
	FastLED.show();
	delay(100);

	for (int i = 0; i<NUM_LEDS; i++){
		leds[i] = CRGB::Black;
	}
	FastLED.show();
	delay(100);}
	
}
```
@AVR8js.sketch(matrix-experiment)

## Questions
### What it does and how it works
Our program is divided into three Parts:

{{1}}
The first part is an alternating pattern of red and a blue lights. This is for the Melbourne Demons, an Australian fotty club who's colours are red and blue.

{{1}}
```cpp Code part 1
for (int i = 0; i<NUM_LEDS; i++){
		if ((i)%2) {
			leds[i] = CRGB::Blue;
		}else{
		leds[i] = CRGB::Red;	
		}
	}
	FastLED.show();
	delay(2021);
	
	for (int j = 0; j < NUM_LEDS; j++)
        { 
         leds[j] = CRGB::Black;

        }
             FastLED.show();
```

{{2}}
The second part is showing the first 50 digits of pi, because why not? Pi is wonderful! These are each shown an obvious length of 3142 ms for 1000ms pi.

{{2}}
```cpp Code part 2
for (int j = 0; j < NUM_LEDS; j++)
        { 
         leds[j] = CRGB::Black;

        }
             FastLED.show();
	
	
	for (int i = 0; i<50; i++) {
		for (int j = 0; j<numbers[i]; j++) {
			leds[j] = CRGB::Green;
 
		}
					            FastLED.show();
		delay(3142);
		for (int j = 0; j < NUM_LEDS; j++)
        { 
         leds[j] = CRGB::Black;

        }
             FastLED.show();
	}
```


{{3}}
The last part is just quick flashing lights, so we could win the award for bringing the most medical harm.

{{3}}
```cpp Code part 3
for (int i = 0; i<500; i++){
	    for (int i = 0; i<NUM_LEDS; i++){
	    	leds[i] = CRGB::White;
	}
	FastLED.show();
	delay(100);

	for (int i = 0; i<NUM_LEDS; i++){
		leds[i] = CRGB::Black;
	}
	FastLED.show();
	delay(100);}
```

### Where the idea came from?

The idea came from Theodor who brought together two of his interests, with the urgent need to create an award winning masterpiece. We aimed for nothing less then all 6 possible awards and less then 4 is most definitely a failure. Even tho the program is still nothing less then brilliant.

### Problems

Due to perfect groupwork, paired with excellent communication, we unexpectedly didn't encounter any problems whatsoever.

### How we wrote the program

With tremendous effort, we overcame incredible difficulties copy and pasting the tutorial code and adapting it to fit our needs.
In a wonderfull dynamic hard work, we were able to implement all of the first fifty digits of pi in our wonderful and highly efficient dataformat, also known as as signed integer array.

### Possible adjustments
Obviously it is tremendously had to find adjustments to such a great working program, unsurprinsingly we couldnt think of improvements in any possible case with our limited ressource in that project.
Alternatively we could think of slight adjustments, for example instead of pi you could use other irrational numbers, i.e. square root 2 or napier constant 'e'. otherwise you could as well use different colours in the beginning to your choosing (maybe your favourite sport team and have some guess the team ;)). Try your luck and if you get very creative and make it marketable, maybe remember our wonderful idea and give us a small piece of your big pie :D. 
Good night lights out. 

# A beautiful Rainbow

!?[](https://cdn.discordapp.com/attachments/1103733215170138277/1103733761713131520/Rainbow.mp4)

Here you can see our beautifully vibrant Rainbow in live action.

## Simulation of a wonderful Rainbow



<div id="matrix-experiment">
<wokwi-neopixel-matrix pin="6" cols="11" rows="1"></wokwi-neopixel-matrix>
<span id="simulation-time"></span>
</div>

<br>

```cpp Rainbow

// Library         
#include "FastLED.h"

// LEDs pin
#define DATA_PIN 6

// LED brightness
#define BRIGHTNESS 180

// Number of LEDs
#define NUM_LEDS 11

// Define the array of leds
CRGB leds[NUM_LEDS];

// Global variable for count
int i = 0;

//Initialize FastLED Library and Set brightness

void setup() {
  FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
  FastLED.setBrightness(BRIGHTNESS);
}

void loop() {
for (i=0; i < NUM_LEDS; i++) // 
    {
    	leds[(i+8) % NUM_LEDS] = CRGB::Red;
    	leds[(i+7) % NUM_LEDS] = CRGB::Orange;
    	leds[(i+6) % NUM_LEDS] = CRGB::Yellow;
    	leds[(i+5) % NUM_LEDS] = CRGB::Green;
    	leds[(i+4) % NUM_LEDS] = CRGB::Aqua;
    	leds[(i+3) % NUM_LEDS] = CRGB::Blue;
    	leds[(i+2) % NUM_LEDS] = CRGB::Purple;
    	leds[(i+1) % NUM_LEDS] = CRGB::Black;
    	leds[(i) % NUM_LEDS] = CRGB::Black;
    	FastLED.show();
    	delay(200);
     
    }

}
```
@AVR8js.sketch(matrix-experiment)


## Documentation of the Rainbow

Rainbow light implementation on an Arduino is a fun and creative project that produces a mesmerizing rainbow color display using an Arduino microcontroller. The implementation involves a sequence of RGB LED lights that change colors in a smooth and continuous pattern.

The idea for this project came from the desire to create a colorful and visually appealing display that could be used for various applications, such as mood lighting, party decorations, or simply for fun. The concept of using RGB LED lights to create a rainbow effect was inspired by the phenomenon of natural rainbows, which display a similar sequence of colors.

The rainbow light implementation on an Arduino works by controlling the amount of red, green, and blue light emitted by each LED to create the desired color. By varying the intensity of each color, the Arduino can produce a transition of colors from red to orange, yellow, green, aqua, blue, and purple, creating a beautiful rainbow effect.

However there were problems to be faced. It took us one semester to study coding on an Arduino. Some of us even got left behind due to burnout. After that we had to learn new methods to connect to the Arduino and upload the code, which resulted in time consuming challenges.

One possible addition to this project could be to add a sound sensor that detects the beat of music and synchronizes the color display with the rhythm. This would enhance the project's entertainment value and make it a great addition to any party or event.

## "Problems of the Rainbow" written by our new employee Mr. ChatGPT

![](https://img.welt.de/img/wirtschaft/mobile244265887/0452509977-ci102l-w1024/Human-AI-robot-with-flowing-binary.jpg)

### long version
However, the journey of implementing the rainbow light on an Arduino was not without its challenges. It took us an entire semester to study and grasp the coding principles required to program the Arduino effectively. Some of us faced burnout along the way, struggling to keep up with the demanding learning curve.

After gaining a solid understanding of Arduino programming, we faced another hurdle – learning new methods to connect to the Arduino and upload the code. This process proved to be time-consuming and presented us with unexpected challenges. It required us to familiarize ourselves with the intricacies of hardware connections, ensuring the components were properly wired and functioning correctly.

Despite the difficulties we encountered, our determination and passion for the project kept us going. We sought assistance from experienced Arduino enthusiasts, delved into online resources, and actively collaborated with one another to troubleshoot issues and find solutions.

With persistence and perseverance, we gradually overcame these obstacles. Our hard work paid off when we successfully uploaded the code to the Arduino and witnessed the mesmerizing display of rainbow colors illuminating the room. The sense of accomplishment we felt was indescribable.

This project taught us the value of patience, dedication, and teamwork. It reinforced the importance of taking breaks and avoiding burnout during the learning process. We also gained valuable knowledge and skills that will undoubtedly benefit us in future endeavors.

In the end, despite the challenges we faced, the beautiful and captivating rainbow light implementation on the Arduino made every hurdle worthwhile. It serves as a testament to our determination, resilience, and the power of creative expression through technology.

### short version

Implementing the rainbow light on an Arduino posed challenges. It took a semester to study Arduino coding, leading to burnout for some. Learning new connection methods and uploading the code proved time-consuming and presented unexpected hurdles. However, perseverance and collaboration helped overcome obstacles, resulting in a mesmerizing rainbow light display. This project taught patience, teamwork, and the power of creative expression through technology.

## Quiz for no reason

What are the colors of our Rainbow?

- [[ ]] red, orange, yellow, lime, green, blue, purple
- [[ ]] red, orange, yellow, green, blue, indigo, purple
- [[X]] red, orange, yellow, green, aqua, blue, purple
- [[ ]] red, gold, yellow, green, aqua, blue, purple 

# Morse Code

**Video**

!?[Video](https://cdn.discordapp.com/attachments/1103717341990240316/1103721158479720470/Morse_code.mp4)

**Presentation**

![Image](https://media.discordapp.net/attachments/1103717341990240316/1103717715467833374/IMG20230427192310.jpg?width=856&height=642)

### Usage

Even though morse code is not as popular for sending messages as it was 130 to 150 years ago, there are still some use cases for this - even though most will not be very practical.

For example, it can be used to learn morse code. You can find out what a message would look like in morse code or try to translate morse code back into the latin alphabet.

### History

The morse code is, although not the oldest, but one of the most simple ways to communicate. It works with only two indicators called „dits“ and „dahs“. These are often visualized using the well known symbols `.` and `-`.

Samuel Morse invented the method to convert entire sentences and numbers into dits & dahs and back, explaining the name of morse code.

Originally morse code was used to communicate over long distances using telegraphs. Typically a button emits an impulse as long as it is pressed. By alternating the duration of those impulses, combinations of dits and dahs can be sent almost everywhere in a matter of milliseconds. If the signal is transmitted using a wire, the receiver just has to connect something that makes the impulses visible, for example a bulb or a speaker.

![Morse Code](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Morsetaste.jpg/800px-Morsetaste.jpg?20170816171722)

### Simulation & Source Code

<div id="matrix-experiment">
<wokwi-neopixel-matrix pin="6" cols="11" rows="1"></wokwi-neopixel-matrix>
<span id="simulation-time"></span>
</div>

<br>

```cpp Morse Code
#include "FastLED.h"
#define DATA_PIN 6
#define BRIGHTNESS 180
#define NUM_LEDS 11

CRGB leds[NUM_LEDS];

// SOURCE: https://morsecode.world/international/timing.html
#define UNIT_MS 200

// LUT for morse code characters.
// Supports all alphanumeric characters.
const char* MORSE_CODE[] = {
  /* A */ ".-",
  /* B */ "-...",
  /* C */ "-.-.",
  /* D */ "-..",
  /* E */ ".",
  /* F */ "..-.",
  /* G */ "--.",
  /* H */ "....",
  /* I */ "..",
  /* J */ ".---",
  /* K */ "-.-",
  /* L */ ".-..",
  /* M */ "--",
  /* N */ "-.",
  /* O */ "---",
  /* P */ ".--.",
  /* Q */ "--.-",
  /* R */ ".-.",
  /* S */ "...",
  /* T */ "-",
  /* U */ "..-",
  /* V */ "...-",
  /* W */ ".--",
  /* X */ "-..-",
  /* Y */ "-.--",
  /* Z */ "--..",
  /* 0 */ "-----",
  /* 1 */ ".----",
  /* 2 */ "..---",
  /* 3 */ "...--",
  /* 4 */ "....-",
  /* 5 */ ".....",
  /* 6 */ "-....",
  /* 7 */ "--...",
  /* 8 */ "---..",
  /* 9 */ "----.",
};

// Takes advantage of the ASCII table to get the index of the character c within the LUT.
int get_alphabet_index(char c) {
  if (c >= 'a' && c <= 'z') {
    return c - 'a';
  } else if (c >= 'A' && c <= 'Z') {
    return c - 'A';
  } else if (c >= '0' && c <= '9') {
    return c - '0' + 26;
  } else {
    return -1;
  }
}

// Makes all LEDs blink in a certain color and for a certain duration (units).
void blink(const unsigned int duration, const CRGB color) {
  fill_solid(leds, NUM_LEDS, color);
  FastLED.show();
  delay(duration * UNIT_MS);
  
  fill_solid(leds, NUM_LEDS, CRGB::Black);
  FastLED.show();
}

// Pause for a certain duration (units).
void pause(const unsigned int duration) {
  delay(duration * UNIT_MS);
}

// Wave animation that plays at the end of a messages.
void repeat_wave() {
  for (int i = 0; i < NUM_LEDS; ++i) {
    leds[i] = CRGB::Red;
    FastLED.show();
    delay(UNIT_MS);
    leds[i] = CRGB::Blue;
    FastLED.show();
  }

  for (int i = NUM_LEDS - 1; i >= 0; --i) {
    leds[i] = CRGB::Red;
    FastLED.show();
    delay(UNIT_MS);
    leds[i] = CRGB::Black;
    FastLED.show();
  }
}

// Displays the given message as morse code.
void run_morse_code(const char* message) {
  for (unsigned int i = 0; i < strlen(message); ++i) {
    char current_character = message[i];

    // Wait for 7 (3 + 3 + 1) units if the current character is a space.
    // Assumes that the message does not start with a space.
    if (current_character == ' ') {
      pause(3);
      continue;
    }

    // Get a string containing the dits and dahs of the current character from the LUT.
    // Continue with the next character if it's not in the LUT.
    unsigned int morse_code_index = get_alphabet_index(current_character);
    if (morse_code_index < 0) continue;
    const char* morse_code = MORSE_CODE[morse_code_index];

    for (unsigned int j = 0; j < strlen(morse_code); ++j) {
      switch (morse_code[j]) {
        case '.':
          // dit: Make LEDs light up in green for 1 unit.
          blink(1, CRGB::Green);
          break;
        case '-':
          // dah: Make LEDs light up in gold for 3 units. 
          blink(3, CRGB::Gold);
          break;
      }

      pause(1);
    }

    pause(3);
  }
}

// Setup LED strip.
void setup() {
  FastLED.addLeds<NEOPIXEL, DATA_PIN>(leds, NUM_LEDS);
  FastLED.setBrightness(BRIGHTNESS);
}

void loop() {
  // Display the message as morse code.
  run_morse_code("SOS");
  delay(500);

  // Run the wave animation.
  repeat_wave();
  delay(500);
}
```
@AVR8js.sketch(matrix-experiment)

The message to display must be written directly into the source code (line 128). It will be transformed into morse code using the official delays and timing.

After the message ends, a sequence of blue and red lights will be shown in order to clearify that the message will restart.


### Quiz

- [ [Hello] (SOS) [Freiberg] (Universitaet) ]
- [ [ ] [ ] [X] [ ] ] `..-. .-. . .. -... . .-. --.`
- [ [ ] [ ] [ ] [X] ] `..- -. .. ...- . .-. ... .. - .- . -`
- [ [X] [ ] [ ] [ ] ] `.... . .-.. .-.. ---`
- [ [ ] [X] [ ] [ ] ] `... --- ...`

