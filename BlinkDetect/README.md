# BlinkDetect
An openCV/dlib based blinking detector that could be used in other projects

## Usage
`import blink`

Run `init()` to initialize camera

Run `eyestate(_args_)` which detects the state of the eye in the latest frame, returning `1` when the eye is opened, `0` when the eye is closed, and `-1` when the eye is undetected.

The arguments for `eyestate(_)` are `eyestate(inputFrame, outputFrame, threshold=4, draw=True`. `inputFrame` is the openCV frame in which the eye is to be detected. `outputFrame` is the Frame where the overlay will be drawn. `threshold` is the eye aspect ratio value that separates eyes being *closed* and *opened*; the default being `4`. `draw` is to enable drawing the overlay of the eye aspect ratio to the frame `outputFrame`.

`stop()` releases the camera from the script and stops detection

Run `python blink.py` for a demo; where pressing `q` on the keyboard stops the program.
