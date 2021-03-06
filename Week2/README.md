### Specification
## `bday.txt`
In [`bday.txt`](https://github.com/ovinnikova/HarvardX-CS50/blob/master/Week2/bday.txt), type the ASCII representation of Happy Birthday, translating its sheet music to the machine-readable representation.

### helpers.c
## `is_rest`
Complete the implementation of is_rest in [helpers.c](https://github.com/ovinnikova/HarvardX-CS50/blob/master/Week2/helpers.c). Recall that blank lines represent rests in our machine-readable format. And recall that synthesize will call this function in order to determine if one of the lines a user has typed in is indeed blank.

## `duration`
Complete the implementation of duration in [helpers.c](https://github.com/ovinnikova/HarvardX-CS50/blob/master/Week2/helpers.c). Recall that this function should take as input as a string a fraction and convert it into some integral number of eighths. You may assume that duration will only be passed a string formatted as X/Y, whereby each of X and Y is a positive decimal digit, and Y is, moreover, a power of 2.

## `frequency`
Finally, complete the implementation of frequency in [helpers.c](https://github.com/ovinnikova/HarvardX-CS50/blob/master/Week2/helpers.c). Recall that this function should take as input as a string a note (e.g., A4) and return its corresponding frequency in hertz as an int.

To compile both notes and synthesize, execute
```
make
```
which should compile both at the same time.

To test your implementation of frequency in helpers.c, execute notes, which calls precisely that function, as via:
```
./notes
```
You can also listen to the outputted notes.wav if you’ve an ear for the notes. Test other octaves by specifying them as command-line arguments, a la:
```
./notes 5
```
To test frequency further, along with is_rest and duration, execute synthesize, as via:
```
./synthesize test.wav
```
Then input one or more notes, one per line, and when done, hit ctrl-d to send EOF ("end of file") to get_string so that it breaks out of that program’s loop. Open the resulting file (e.g., test.wav) by executing
```
open test.wav
```
To pass all of the notes in bday.txt into synthesize at once, execute:
```
./synthesize bday.wav < bday.txt
```
Then execute
```
open bday.wav
```
