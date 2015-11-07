# Hexadecimal RGB Values to Decimal RGB Values in Stata
This is a utility program that converts hexadecimal RGB encoded colors into decimal values.  It takes a sole argument which can be either a string value or a variable.  If a variable is passed to the program, it returns the RGB values in a new variable called rgb.  If string values are passed to the program it will print a table showing the individual component values, a comma separated RGB value, and a Stata formatted RGB string.


```
// Convert the color palette from d3.scale.category10() to RGB values
. hextorgb, hex("#1f77b4" "#ff7f0e" "#2ca02c" "#d62728" "#9467bd" "#8c564b" "#e377c2" "#7f7f7f" "#bcbd22" "#17becf")
________________________________________________________________________________
          Red       Green     Blue      RGB               RGB String                 
________________________________________________________________________________

          226      56        27        226, 56, 27       "226 56 27"
          240      232       196       240, 232, 196     "240 232 196"
          146      10        146       146, 10, 146      "146 10 146"
          49       51        66        49, 51, 66        "49 51 66"
          25       55        180       25, 55, 180       "25 55 180"
          152      41        125       152, 41, 125      "152 41 125"
          23       56        16        23, 56, 16        "23 56 16"
          232      232       232       232, 232, 232     "232 232 232"
          155      180       6         155, 180, 6       "155 180 6"
          50       207       237       50, 207, 237      "50 207 237"
________________________________________________________________________________


// Displays the returned local macros when string values are passed to the argument
. ret li

macros:
         r(rgbcomma10) : "50, 207, 237"
              r(rgb10) : "50 207 237"
             r(blue10) : "237"
            r(green10) : "207"
              r(red10) : "50"
          r(rgbcomma9) : "155, 180, 6"
               r(rgb9) : "155 180 6"
              r(blue9) : "6"
             r(green9) : "180"
               r(red9) : "155"
          r(rgbcomma8) : "232, 232, 232"
               r(rgb8) : "232 232 232"
              r(blue8) : "232"
             r(green8) : "232"
               r(red8) : "232"
          r(rgbcomma7) : "23, 56, 16"
               r(rgb7) : "23 56 16"
              r(blue7) : "16"
             r(green7) : "56"
               r(red7) : "23"
          r(rgbcomma6) : "152, 41, 125"
               r(rgb6) : "152 41 125"
              r(blue6) : "125"
             r(green6) : "41"
               r(red6) : "152"
          r(rgbcomma5) : "25, 55, 180"
               r(rgb5) : "25 55 180"
              r(blue5) : "180"
             r(green5) : "55"
               r(red5) : "25"
          r(rgbcomma4) : "49, 51, 66"
               r(rgb4) : "49 51 66"
              r(blue4) : "66"
             r(green4) : "51"
               r(red4) : "49"
          r(rgbcomma3) : "146, 10, 146"
               r(rgb3) : "146 10 146"
              r(blue3) : "146"
             r(green3) : "10"
               r(red3) : "146"
          r(rgbcomma2) : "240, 232, 196"
               r(rgb2) : "240 232 196"
              r(blue2) : "196"
             r(green2) : "232"
               r(red2) : "240"
          r(rgbcomma1) : "226, 56, 27"
               r(rgb1) : "226 56 27"
              r(blue1) : "27"
             r(green1) : "56"
               r(red1) : "226"

// Can also handle larger string values (in this case it is d3.scale.category20()
. hextorgb, hex("#1f77b4" "#aec7e8" "#ff7f0e" "#ffbb78" "#2ca02c" "#98df8a" "#d62728" "#ff9896" "#9467bd" "#c5b0d5" "#8c564b" "#c49c94" "#e377c2" "#f7b6d2" "#7f7f7f" "#c7c7c7" "#bcbd22" "#dbdb8d" "#17becf" "#9edae5")
________________________________________________________________________________
          Red       Green     Blue      RGB               RGB String                 
________________________________________________________________________________

          226      56        27        226, 56, 27       "226 56 27"
          206      61        78        206, 61, 78       "206 61 78"
          240      232       196       240, 232, 196     "240 232 196"
          240      132       71        240, 132, 71      "240 132 71"
          146      10        146       146, 10, 146      "146 10 146"
          73       238       108       73, 238, 108      "73 238 108"
          49       51        66        49, 51, 66        "49 51 66"
          240      73        45        240, 73, 45       "240 73 45"
          25       55        180       25, 55, 180       "25 55 180"
          37       11        38        37, 11, 38        "37 11 38"
          152      41        125       152, 41, 125      "152 41 125"
          28       153       25        28, 153, 25       "28 153 25"
          23       56        16        23, 56, 16        "23 56 16"
          64       47        17        64, 47, 17        "64 47 17"
          232      232       232       232, 232, 232     "232 232 232"
          61       61        61        61, 61, 61        "61 61 61"
          155      180       6         155, 180, 6       "155 180 6"
          134      134       177       134, 134, 177     "134 134 177"
          50       207       237       50, 207, 237      "50 207 237"
          205      113       39        205, 113, 39      "205 113 39"
________________________________________________________________________________

```

