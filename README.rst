

Magics automatic styling library 
=================================

An automatic contour selection is implemented in Magics. When chosen, Magics will try to detect which parameter is being plotted and apply a predefined style.

.. code:: python
	mcont(contour_automatic_setting = "ecmwf") 

Magics Definition files
-----------------------

Magics will browse the directories define in the environment variable  **MAGICS_STYLE_PATH**.
Note that if *ecmwf* is found in   **MAGICS_STYLE_PATH**, it will be interpreted as the default magics library path. 

If a directory contains a file *styles.json*, Magics will interpret it as a library of styles.
Here is an example :
.. code:: json 
{
    "tourism-index-style" :
      {
        "contour" :  "off",
        "contour_shade" :  "on",
        "contour_level_selection_type"  :  "list",
        "contour_level_list": "0.0/0.1/0.2/0.3/0.4/0.5/0.6/0.7/0.8/0.9/1.",
        "contour_interpolation_floor" : 0.00,
        "contour_interpolation_ceiling" : 1.00,
        "contour_shade_method" : "area_fill",
        "contour_shade_colour_method" : "palette",
        "contour_shade_palette_name" : "m_orange_purple_10"
      }
}

Where *tourism-index-style* is the name of the style and the dictionary attached to it the list of the Magics parameters to apply when using this style.



.. code:: json
[
  {
    "styles": [
      "tourism-index-style"
    ],
    "match": [
      {
        "standard_name": "cit-proj",
        "units": "1"
      }
    ]
  }
]







License
-------

Copyright 2017-2018 European Centre for Medium-Range Weather Forecasts (ECMWF).

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at: http://www.apache.org/licenses/LICENSE-2.0.
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
