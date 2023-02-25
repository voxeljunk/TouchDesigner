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
- MIDI Learn mode detects MIDI channel and sets CC and Note range start to most recently received CC and note values
- external CC and Note inputs for bypassing internal MIDI mapper
- one-click Parameter Setup to scan for all custom numeric, button, toggle and momentary parameters in parent COMP
- Autobind mode for instant binding to selected parent paremeters
- auto-scales MIDI CCs to corresponding parent parameter's min/max ranges using internal Animation COMP
- MIDI note to toggle converter with string field for fast, intuitive control conversion
- daisy chain I/O for easy control over multiple instances of a single parent effect or processor
- merged output with MIDI-controlled + all other parent params and lag CHOP for subtle control smoothing

### Basic Usage
1. place MIME inside any COMP you'd like to control with MIDI.
2. press Setup button to detect MIDI devices and generate a list of the Parent COMP's custom parameters and their designated min/max control ranges.
3. select your MIDI device with the Device ID slider.
4. activate MIDI Learn mode and send the first CC and Note in your desired control range.
5. use the MIDI CC and Note Parameter Select fields to choose which parameters to map your MIDI controller to.

that's it! now you're ready to go!

### Advanced Usage - Control Smoothing and Daisy Chaining
the above method maps directly to parent parameters. if those parameters are already mapped as you like then that's all you need to do. however, MIME features three outputs past the mapping script which enable daisy-chaining and global smoothing. these outputs are as follows:
- **params** - all parameters with smoothing (lag) applied. the lag amount is controlled by the Control Smoothing parameter. great for mapping numeric parameters.
- **params_nosmoothing** - all parameters without lag applied. best used to map to menus and other controls which don't really benefit from smoothing.
- **daisy_chain_out** - same as **params_nosmoothing** but tapped before **daisy_chain_input**.

to make the most of these features, connect null CHOPs to MIME's **params** and **params_nosmoothing** outputs and use these when making any expression mappings inside your COMP. connect an in CHOP to the **daisy_chain_in** and an out CHOP to the **daisy_chain_out** for quick connection of multiple identical COMPs in series. please note that the parameter controls in daisy-chained devices will not track signals from their daisy chain inputs. only MIME's outputs reflect these changes.

---
### Version History

#### v0.4 // 2/24/23
- added MIDI Learn Modes - default "Auto-Off" mode automatically deactivates MIDI Learn after a user-definable interval (default 10s)
- added MIDI mute and MIDI Value Reset parameters
- improved MIDI device scanning
- added external control merge input - useful in certain cases where alternative control schemes are desired in the absence of a MIDI controller

#### v0.3 // 2/12/23
- fixed a bug in parameter pickup script. please note that parameter pickup does not play nice with expressions meaning if you have pickup active you will likely not be able to quickly type expressions into parameter fields on the parent. as such pickup is off by default but is still available as it may be handy in certain use cases.

#### v0.2 // 2/11/23
- experimental build with smart parameter pickup. haven't tested this much yet, hope it doesn't break anything too bad 😬 added a MIDI Pickup toggle just in case.
- replaced Device ID slider with menu
- added a bunch of Parameter Help data

#### v0.1 // 2/10/23
- initial release

---
<sub>title art made with [TAAG](https://patorjk.com/software/taag/) using the [Slant Relief](https://patorjk.com/software/taag/#p=author&f=Slant%20Relief&t=MIME) font</sub>
