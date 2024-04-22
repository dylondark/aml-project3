# AML Project III
This project, completed by Luke Gegick, Dylan Miller, and Jackson Dockerty, uses different machine learning
methods to predict the type of eclipse given its features

# Features (Highlighted features are included)
<mark> Delta T(s) </mark>- The discrepancy in seconds between Terrestrial Time (TT) and Universal Time (UT) <br>
<mark> Lunation Number </mark>- An enumeration system for identifying lunar months <br>
<mark> Saros Number </mark>- Identifies the eclipse cycle, a period of approximately 18 years <br>
<mark> Gamma </mark>- Measures how centrally the moon's shadow passes across Earth <br>
<mark> Eclipse Magnitude </mark>- Fraction of the Sun's diameter obscured by the Moon at the maximum point of the eclipse <br>
<mark> Sun Altitude </mark>- The suns angular elevation above the horizon as observed from a specific location on Earth <br>
<mark> Sun Azimuth </mark>- the suns angular position along the horizon <br>
<mark> Path Width (km) </mark>-  width of the region on Earth's surface where the lunar eclipse is visible <br>
<mark> Year </mark>- The year the eclipse occurs <br>
<mark> Month </mark>- the Month the eclipse occurs <br>
<mark> Day </mark>- The day of the month the eclipse occurs <br>
<mark> Eclipse Latitude </mark>- the angular distance of the Moon from the Earth's equatorial plane <br>
<mark> Eclipse Longitude </mark>- the longitudinal position of the Moon at the time of the eclipse <br>
<mark> obliquity </mark>- the tilt of the Earth's axis relative to its orbital plane around the Sun <br>
<mark> Inter-Eclipse Duration </mark>- the length of time between successive lunar eclipses <br>
<mark> Visibility Score </mark> -  the score of how visible the eclipse is between 0 and 1<br>
<mark> Moon Distance (km) </mark> - the distanc of the moon from Earth in km  <br>
<mark> Sun Distance (km) </mark> - the distance of the sun from Earth in km <br>
<mark> Moon Angular Diameter (degrees) </mark> - The angular diameter of the moon in degrees <br>
<mark> Sun Angular Diameter (degrees) </mark> - The angular diameter of the sun in degrees <br>
<mark> Central Duration Seconds </mark>- the duration of time during which the Moon remains fully immersed within the Earth's umbral shadow <br>
<mark> Normalized Duration </mark> - the normalized duration of the eclipse <br>
<mark> Normalized Path Width </mark> - the normalized path width of the eclipse <br>
<mark> EII </mark>- This index is a measure used to quantify the quality and significance of information <br>
<mark> HEAS </mark> - the Heliocentric Earth Angular Size data <br>
<mark> Localized ESC </mark> - the Localized Eclipse Start Coordinates <br>
<mark> Eclipse Interval </mark> -  the time period between consecutive occurrences of a specific type of eclipse <br>
Catalog Number (DROP) <br>
Calender Date (DROP) <br>
Eclipse Time (DROP) <br>
Latitude (DROP) <br>
Longitude (DROP) <br>
Central Duration (DROP) <br>
Date Time (DROP) <br>
Visibility (DROP) <br>
Geographical Hemisphere (DROP) <br>
Daytime/Nighttime (DROP) <br>
Sun Constellation (DROP) <br>
Eclipse Classification (DROP) <br>
Duration in Seconds (DROP) <br>
Year Modulus (DROP) <br>
Decade (DROP) <br>
ESC Moving Average (DROP) <br>
ESC Wide-Scale Moving Average (DROP) <br>
Cluster (DROP) <br>
Cluster 6 (DROP) <br>

# Predict (Independant Variable)
Eclipse Type - Type of solar eclipse (Total, Annular, Hybrid, or Partial)

# Key (Independant Variable)
- <strong> Eclipse type </strong>
    - T = 0 
        - (Total solar eclipse)
    - Tm = 1 
        - (Middle of a total eclipse - marks midpoint of a total solar eclipse)
    - Ts = 2 
        - (Total Solar Eclipse (third contact) - Marks the end of totality during a total solar eclipse)
    - T+ = 3 
        - (Partial Phase of a Total Solar Eclipse (post-total) - partial phases of a total solar eclipse after totality)
    - T- = 4 
        - (Partial Phase of a Total Solar Eclipse (pre-total) - partial phases of a total solar eclipse before totality)
    - Tn = 5
        - Terminating Node" refers to the point during an eclipse cycle when the moon's shadow first touches the Earth
    - A = 6 
        - (Annular Solar Eclipse - Moon passes in front of the Sun but does not completely cover it)
    - As = 7 
        - (Annular Solar Eclipse (third contact) - the end of annularity)
    - Am = 8 
        - (Middle of an Annular Solar Eclipse - the midpoint of an annular solar eclipse)
    - A+ = 9 
        - (Partial Phase of an Annular Solar Eclipse (post-annular) - partial phases of an annular solar eclipse after the annular phase)
    - A- = 10 
        - (Partial Phase of an Annular Solar Eclipse (pre-annular) - partial phases of an annular solar eclipse before the annular phase)
    - An = 11 
        - "Ascending Node" refers to the point where the moon's path (orbit) intersects with the ecliptic plane 
    - P = 12
        - (Partial Solar Eclipse)
    - Pb = 13
        - (Partial Solar Eclipse (beginning))
    - Pe = 14
        -  (Partial Solar Eclipse (end))
    - H = 15
        - (Hybrid Solar Eclipse)
    - Hm = 16
        - (Middle of a Hybrid Solar Eclipse)
    - H2 = 17
        - (Hybrid Solar Eclipse (second contact))
    - H3 = 18
        - (H3: Hybrid Solar Eclipse (third contact))

# Implementation Notes
- Drop categories who do not have a value in Centralized Duration Seconds to test how it affects accuracy versus imputing
    - The normalized data fields and centralized duration fields all have the same id for unfilled data so do not drop for each, only drop with respect to one data column to save performance
