cycloidal
=========

![ScreenShot](https://raw.github.com/mikedh/cycloidal/master/images/cycloidal_example.png)

Generate profiles for [cycloidal drives](https://en.wikipedia.org/wiki/Cycloidal_drive), a very cool reducer mechanism. They're popular in machine tools and robotics due to relative ease of fabrication, high ratios, decent efficiency, and ability to survive high shock loads. 

The profile generation was implemented from 'Gear geometry of cycloid drives', Chen BingKui et al.' and inspired by a [post on zincland](http://www.zincland.com/hypocycloid). 

Install requirements with:

```
pip install trimesh[easy] matplotlib
```

Run with:

```json5:configure.json5
{
	radius_pin: 2.5,
	count_pin: 13,
	// Radius for positioning of "radius_pin"
	radius_pattern: 30,

	input_radius: 6,
	input_count: 6,
	// It's good for 1/2 or 2/3 of "radius_pattern"
	input_pattern: 20,

	// set eccentricity as a fraction of pin radius
	eccentricity: 1.4,
}
```

```bash
ipython cycloidal.py configure.json5
```