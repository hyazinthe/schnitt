# Project schnitt
* voice activity detector (VAD) algorithm for splitting sound files
* Java Swing GUI for visualization, error analysis and editing
* group project for my MA programming course (Fall, 2015, Kobe University)


### Wave panel
  * editable <tt>hypo</tt> tier (green)
  * non-editable <tt>target</tt> tier (dark blue)
  * automatically updating <tt>eval</tt> tier (red) with VAD errors
  
![wav panel](https://github.com/kinokocchi/schnitt/blob/master/doc/wavpanel_20151127.png)

Type  | Description
------|------------------------------------------------------
TN    |true negative; silence detected as silence
TN    |true positive; speech detected as speech
WC    |word clipping 
NDS(1)|noise detected as speech, during silence
NDS(2)|noise detected as speech, arching 2 speech activities
FEC 	|front end clipping
REC 	|rear end clipping
HEAD 	|overhead: hypo starts before voice activity
TAIL 	|tail: hypo ends after voice activity ends


### Evaluation 
The following FDA (more precisely Finite State Transducer) is implemented.
![wav panel](https://github.com/kinokocchi/schnitt/blob/master/doc/vad-trans.png)



