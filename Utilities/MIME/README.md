```                                                   
__/\\\\____________/\\\\__/\\\\\\\\\\\__/\\\\____________/\\\\__/\\\\\\\\\\\\\\\_        
 _\/\\\\\\________/\\\\\\_\/////\\\///__\/\\\\\\________/\\\\\\_\/\\\///////////__       
  _\/\\\//\\\____/\\\//\\\_____\/\\\_____\/\\\//\\\____/\\\//\\\_\/\\\_____________      
   _\/\\\\///\\\/\\\/_\/\\\_____\/\\\_____\/\\\\///\\\/\\\/_\/\\\_\/\\\\\\\\\\\_____     
    _\/\\\__\///\\\/___\/\\\_____\/\\\_____\/\\\__\///\\\/___\/\\\_\/\\\///////______    
     _\/\\\____\///_____\/\\\_____\/\\\_____\/\\\____\///_____\/\\\_\/\\\_____________   
      _\/\\\_____________\/\\\_____\/\\\_____\/\\\_____________\/\\\_\/\\\_____________  
       _\/\\\_____________\/\\\__/\\\\\\\\\\\_\/\\\_____________\/\\\_\/\\\\\\\\\\\\\\\_ 
        _\///______________\///__\///////////__\///______________\///__\///////////////__
```
## MIDI Input Management Expert
#### by [voxeljunk](https://linktr.ee/voxeljunk)
a one-stop shop for MIDI CC/note detection, selection, scaling and binding.
- MIDI Learn mode detects MIDI channel and sets CC and Note range start to last received CC and note values
- external CC and Note inputs for bypassing internal MIDI mapper
- one-click Parameter Setup to scan for all custom numeric, button, toggle and momentary parameters in parent COMP
- Autobind mode for instant binding to selected parent paremeters
- auto-scales MIDI CCs to corresponding parent parameter's min/max ranges using internal Animation COMP
- MIDI note to toggle converter with string field for fast, intuitive control conversion
- daisy chain I/O for easy control over multiple instances of a single parent effect or processor
- merged output with MIDI-controlled + all other parent params and lag CHOP for subtle control smoothing

### Usage
1. place MIME inside any COMP you'd like to control with MIDI.
2. press  Setup button to detect MIDI devices and generate a list of the Parent COMP's custom parameters and their designated min/max control ranges.
3. select your MIDI device with the Device ID slider.
4. activate MIDI Learn mode and send the first CC and/or Note in your desired control range. don't forget to turn off MIDI Learn when you're done!
5. use the MIDI CC and Note Parameter Select fields to choose which parameters to map your MIDI controller to.

that's it! now you're ready to go!

---
### Version History

#### v0.2 // 2/11/23
- experimental build with smart parameter pickup. haven't tested this much yet, hope it doesn't break anything too bad 😬 added a MIDI Pickup toggle just in case.
- replaced Device ID slider with menu
- added a bunch of Parameter Help data

#### v0.1 // 2/10/23
initial release

---
<sub>title art made with [TAAG](https://patorjk.com/software/taag/) using the [Slant Relief](https://patorjk.com/software/taag/#p=author&f=Slant%20Relief&t=MIME) font</sub>
