# ScArcGauge
This class is a specialized to create an arc.
By default the arc create a closed circle: from 0° to 360°.
Note that all angle is usually expressed in degrees and almost methods need to have an delta angle relative to the start angle.

This class extend the [ScGauge](..\sc-gauge\ScGauge.md) class.
This class inherit all its properties from the [ScGauge](..\sc-feature\ScGauge.md) so please take a look to the related documentation.


#### Public methods

- **float percentageToAngle(float percentage)**<br />
Convert a percentage value in a angle (in degrees) value respect the start and sweep angles.


#### Getter and Setter

- **get/setAngleStart**  -> `float` value, default `0`<br />
The start angle in degrees.

- **get/setAngleSweep**  -> `float` value, default `360`<br />
The sweep angle (in degrees) is the delta value between the start angle and the end angle.
This is limited angle: from -360° to 360°.
Values over the limits will be normalized to the limit.


---
####### XML using

<img align="right" src="https://github.com/Paroca72/sc-widgets/blob/master/raw/scarc/5.jpg"> 
```xml
    <com.sccomponents.widgets.ScArc
        android:layout_width="200dp"
        android:layout_height="wrap_content"
        android:padding="10dp"
    />
```


####### XML Properties
```xml
    <declare-styleable name="ScComponents">
        ...
        <attr name="scc_angle_start" format="float" />
        <attr name="scc_angle_sweep" format="float" />
    </declare-styleable>
```


---
####### Let's play

<img src="https://github.com/Paroca72/sc-widgets/blob/master/raw/sc-arc/1.jpg" align="right" />
Basic
```xml
    <com.sccomponents.widgets.ScArc
        android:layout_width="300dp"
        android:layout_height="300dp"
        android:padding="10dp"
        android:background="#f5f5f5"/>
```

<img src="https://github.com/Paroca72/sc-widgets/blob/master/raw/sc-arc/2.jpg" align="right" />
All feature in basic mode
```xml
    <com.sccomponents.widgets.ScArcGauge
        android:layout_width="300dp"
        android:layout_height="wrap_content"
        android:padding="30dp"
        android:background="#f5f5f5"
        sc:scc_angle_start="135"
        sc:scc_angle_sweep="270"
        sc:scc_stroke_size="6dp"
        sc:scc_progress_size="4dp"
        sc:scc_value="45"
        sc:scc_notchs="8"
        sc:scc_notchs_length="10dp"
        sc:scc_text_tokens="01|02|03|04|05|06|07|08"
        sc:scc_pointer_radius="10dp"
        />
```

---
####### Examples

Press on the picture linked below to see the demonstration.

[![image](https://github.com/Paroca72/sc-widgets/blob/master/raw/sc-arcgauge/f-01.jpg)](flat.md)
[![image](https://github.com/Paroca72/sc-widgets/blob/master/raw/sc-arcgauge/f-02.jpg)](flat.md)
[![image](https://github.com/Paroca72/sc-widgets/blob/master/raw/sc-arcgauge/i-01.jpg)](indicator.md)


# License
<pre>
 Copyright 2015 Samuele Carassai

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in  writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,  either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
</pre>