# Fourier Scene Tutorial

### Tsymbol20vectors
```python
class Tsymbol20vectors(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 20,
        "run_time": 10, # 10 seconds
        "tex_class": TextMobject,
        "tex": "T",
    }
```
<p align="center"><img src ="/gifs/Tsymbol20vectors.gif" /></p>

### Tsymbol50vectors
```python
class Tsymbol50vectors(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 50,
        "run_time": 10, # 10 seconds
        "tex_class": TextMobject,
        "tex": "T"
    }
```
<p align="center"><img src ="/gifs/Tsymbol50vectors.gif" /></p>

### Tsymbol150vectors
```python
class Tsymbol150vectors(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 150,
        "run_time": 10, # 10 seconds
        "tex_class": TextMobject,
        "tex": "T"
    }
```
<p align="center"><img src ="/gifs/Tsymbol150vectors.gif" /></p>

### SigmaSymbol150vectors
```python
class SigmaSymbol150vectors(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 150,
        "run_time": 10, # 10 seconds
        "tex_class": TexMobject, # <-------- Default
        "tex": "\\Sigma"
    }
```
<p align="center"><img src ="/gifs/SigmaSymbol150vectors.gif" /></p>

### SlowFactor0_1
```python
class SlowFactor0_1(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "run_time": 7,
        "tex_class": TexMobject,
        "tex": "\\Sigma",
        "slow_factor": 0.1, # <------------------ Default
    }
```
<p align="center"><img src ="/gifs/SlowFactor0_1.gif" /></p>

### SlowFactor0_3
```python
class SlowFactor0_3(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "run_time": 7,
        "tex_class": TexMobject,
        "tex": "\\Sigma",
        "slow_factor": 0.3, # <------------------
    }
```
<p align="center"><img src ="/gifs/SlowFactor0_3.gif" /></p>

### SlowFactor0_5
```python
class SlowFactor0_5(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "run_time": 7,
        "tex_class": TexMobject,
        "tex": "\\Sigma",
        "slow_factor": 0.5, # <------------------
    }
```
<p align="center"><img src ="/gifs/SlowFactor0_5.gif" /></p>

### StartDrawTrue
```python
class StartDrawTrue(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 15,
        "tex": "\\tau",
        "start_drawn": True # <------------------ Default
    }
```
<p align="center"><img src ="/gifs/StartDrawTrue.gif" /></p>

### StartDrawFalse
```python
class StartDrawFalse(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 15,
        "tex": "\\tau",
        "start_drawn": False # <------------------
    }
```
<p align="center"><img src ="/gifs/StartDrawFalse.gif" /></p>

### InterpolateConfig0to1
```python
class InterpolateConfig0to1(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 15,
        "tex": "\\tau",
        "interpolate_config": [0, 1] # <---------- Default
    }
```
<p align="center"><img src ="/gifs/InterpolateConfig0to1.gif" /></p>

### InterpolateConfig0_3to_1
```python
class InterpolateConfig0_3to_1(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 15,
        "tex": "\\tau",
        "interpolate_config": [0.3, 1] # <---------- 
    }
```
<p align="center"><img src ="/gifs/InterpolateConfig0_3to_1.gif" /></p>

### InterpolateConfig1_to_1
```python
class InterpolateConfig1_to_1(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 15,
        "tex": "\\tau",
        "interpolate_config": [1, 1] # <---------- # always write
    }
```
<p align="center"><img src ="/gifs/InterpolateConfig1_to_1.gif" /></p>

### NCyclesVsRunTime
```python
class NCyclesVsRunTime(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "n_cycles": 3,
        "tex": "\\tau",
    }
```
<p align="center"><img src ="/gifs/NCyclesVsRunTime.gif" /></p>

### WaitBeforeStart
```python
class WaitBeforeStart(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "n_cycles": 1,
        "tex": "\\tau",
        "wait_before_start": 2
    }
```
<p align="center"><img src ="/gifs/WaitBeforeStart.gif" /></p>

### CenterPoint
```python
class CenterPoint(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "n_cycles": 1,
        "tex": "\\tau",
        "center_point": RIGHT*3
    }
```
<p align="center"><img src ="/gifs/CenterPoint.gif" /></p>

### CustomPosition
```python
class CustomPosition(FourierOfTexSymbol):
    CONFIG = {
        "n_vectors": 30,
        "n_cycles": 1,
        "tex": "\\tau",
        "center_point": RIGHT*3,
        "path_custom_position": lambda mob: mob.to_edge(LEFT),
        "circle_config": {
            "stroke_opacity": 0,
        },
    }
```
<p align="center"><img src ="/gifs/CustomPosition.gif" /></p>

---------------------

```python
class FourierFromSVG(AbstractFourierFromSVG):
    CONFIG = {
        # if start_draw = True the path start to draw
        "start_drawn": True,
        # SVG file name
        "file_name": None,
        "svg_config": {
            "fill_opacity": 0,
            "stroke_color": WHITE,
            "stroke_width": 1,
            "height": 7
        },
        # Draw config
        "drawn_path_color": YELLOW,
        "interpolate_config": [0, 1],
        "n_vectors": 50,
        "big_radius": 2,
        "drawn_path_stroke_width": 2,
        "center_point": ORIGIN,
        # Duration config
        "slow_factor": 0.1,
        "n_cycles": None,
        "run_time": 10,
        # colors of circles
        "colors": [
            BLUE_D,
            BLUE_C,
            BLUE_E,
            GREY_BROWN,
        ],
        # circles config
        "circle_config": {
            "stroke_width": 1,
        },
        # vector config
        "vector_config": {
            "buff": 0,
            "max_tip_length_to_length_ratio": 0.25,
            "tip_length": 0.15,
            "max_stroke_width_to_length_ratio": 10,
            "stroke_width": 1.7,
        },
        "base_frequency": 1,
        # definition of subpaths
        "parametric_function_step_size": 0.001,
    }
```

### SVGDefault
```python
class SVGDefault(FourierFromSVG):
    CONFIG = {
        "n_vectors": 100,
        "n_cycles": 1,
        "file_name": "c_clef", # in assets/svg_images/c_clef.svg
    }
```
<p align="center"><img src ="/gifs/FourierFromSVG.gif" /></p>

### ZoomedActivate
```python
class ZoomedActivate(FourierFromSVG):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 50,
        "n_cycles": 1,
        "file_name": "c_clef",
        "include_zoom_camera": True,
        "zoom_position": lambda zc: zc.to_corner(DR)
    }
```
<p align="center"><img src ="/gifs/ZoomedActivate.gif" /></p>

### ZoomedConfig
```python
class ZoomedConfig(FourierFromSVG):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 150,
        "n_cycles": 1,
        "file_name": "c_clef",
        "path_custom_position": lambda path: path.shift(LEFT*2),
        "center_point": LEFT*2,
        "circle_config": {
            "stroke_width": 0.5,
            "stroke_opacity": 0.2,
        },
        # Zoom config
        "include_zoom_camera": True,
        "zoom_position": lambda zc: zc.to_edge(RIGHT).set_y(0),
        "zoom_factor": 0.5,
        "zoomed_display_height": 5,
        "zoomed_display_width": 5,
        "zoomed_camera_config": {
            "default_frame_stroke_width": 3,
            "cairo_line_width_multiple": 0.05,
            # What is cairo_line_width_multiple?
            # See here: https://stackoverflow.com/questions/60765530/manim-zoom-not-preserving-line-thickness
        },
    }
```
<p align="center"><img src ="/gifs/ZoomedConfig.gif" /></p>

### ZoomedDisplayToFullScreen
```python
class ZoomedDisplayToFullScreen(FourierOfTexSymbol):
    CONFIG = {
        "slow_factor": 0.05,
        "n_vectors": 30,
        "run_time": 16,
        "tex": "\\tau",
        # Zoom config
        "include_zoom_camera": True,
        "zoom_position": lambda zc: zc.to_corner(DR),
        # Zoomed display to Full screen config
        "scale_zoom_camera_to_full_screen": True,
        "scale_zoom_camera_to_full_screen_at": 4, # Move the camera at 4 seconds
        "zoom_camera_to_full_screen_config": {
            "run_time": 3,
            "func": smooth,
            "velocity_factor": 1
        },
    }
```
<p align="center"><img src ="/gifs/ZoomedDisplayToFullScreen.gif" /></p>

### ZoomedDisplayToFullScreenWithRestore
```python
class ZoomedDisplayToFullScreenWithRestore(ZoomedDisplayToFullScreen):
    CONFIG = {
        "run_time": 20,
        "zoom_camera_to_full_screen_config": {
            "run_time": 12,
            "func": lambda t: there_and_back_with_pause(t, 1/10),
            # learn more: manimlib/utils/rate_functions.py
        },
    }
```
<p align="center"><img src ="/gifs/ZoomedDisplayToFullScreenWithRestore.gif" /></p>

-----------------------
### FourierOfPathsTB
```python
class FourierOfPathsTB(FourierOfPaths):
    CONFIG = {
        "n_vectors": 100,
        "tex_class": TextMobject,
        "tex": "TB",
        "tex_config": {
            "stroke_color": RED,
        },
        "time_per_symbol": 5,
        "slow_factor": 1 / 5,
    }
```
<p align="center"><img src ="/gifs/FourierOfPathsTB.gif" /></p>

### FourierOfPathsSVG
```python
class FourierOfPathsSVG(FourierOfPaths):
    CONFIG = {
        "n_vectors": 100,
        "file_name": "music_symbols",
        "svg_config": {
            "stroke_color": RED,
        },
        "time_per_symbol": 5,
        "slow_factor": 1 / 5,
    }
```
<p align="center"><img src ="/gifs/FourierOfPathsSVG.gif" /></p>
