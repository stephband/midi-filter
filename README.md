# midi-filter

Filters browser MIDI events.


## Instantiation

Create a filter:

    var midiFilter = new MIDIFilter(options);

This creates a filter node.
The <code>new</code> keyword is optional.


### .in(message)

To filter MIDI messages, call the filter's <code>in</code> method:

    midiFilter.in(message);


### .out(fn)

To listen to the output, register a listener with the filter's <code>out</code> method:

    midiFilter.out(fn);

The callback function <code>fn</code> will be called whenever a MIDI message matches
the filter options.


## Options

A filter understands the options:

    {
        port:    number | string
        channel: number (1-16) | fn
        message: string (message type) | fn
        data1:   number (0-127) | fn
        data2:   number (0-127) | fn
    }

Functions should return a boolean.