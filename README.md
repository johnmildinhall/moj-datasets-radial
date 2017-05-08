# moj-datasets-radial

A D3.js interactive radial visualisation of Justice System datasets and how they connect to each other. 

## Getting started

Clone the repo and use a simple Python server:

``` python -m SimpleHTTPServer 8000 ```

Then navigate to http://localhost:8000/radial.html . 

there are some experimental visualisations also:

http://localhost:8000/radial2.html
http://localhost:8000/tree.html

## Recalculating the connections

The raw data is held in raw-data2.csv. This is transformed into JSON by using 

``` node data-processing.js ```

This is calculated by taking column B, which is "From", and separating all the values in column D, which is "To". 

If you make changes to the raw data you need to be careful to make sure that each reference in column D corresponds to a value in column B. Any ommissions, or any spelling mistakes will cause the visualisation to break.