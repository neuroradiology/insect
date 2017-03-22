insect
======

A fast, repl-style scientific calculator for the web and for the terminal.

[![insect](media/insect-32x32.png)](https://shark.fish/insect/)

* [**Web version**](https://shark.fish/insect/)
* [Terminal version](#install)

Features
--------
- Evaluation of mathematical expressions:
  ```
  1920/16*9
  2^32
  sqrt(1.4^2 + 1.5^2) * cos(pi/3)^2
  ```
  Supported functions: `acos`, `acosh`, `asin`, `asinh`, `atan`, `atanh`,
  `ceil`, `cos`, `cosh`, `exp`, `floor`, `ln`, `log`, `log10`, `round`, `sin`,
  `sinh`, `sqrt`, `tan`, `tanh`.

- Parsing and handling of physical units:
  ```
  2min + 30s
  40kg * 9.8m/s² * 150cm
  sin(30°)
  ```
  Supported units: `A`, `B`, `Bq`, `Byte`, `Bytes`, `C`, `F`, `Gy`, `H`, `Hz`, `J`, `K`, `L`, `N`, `Pa`, `S`, `Sv`, `T`, `V`, `W`, `Wb`, `ampere`, `becquerel`, `bit`, `bits`, `bps`, `byte`, `bytes`, `candela`, `cd`, `coulomb`, `d`, `day`, `days`, `deg`, `degree`, `degrees`, `eV`, `electronvolt`, `farad`, `feet`, `foot`, `ft`, `g`, `gram`, `grams`, `gray`, `h`, `ha`, `hectare`, `henry`, `hertz`, `hour`, `hours`, `in`, `inch`, `inches`, `joule`, `joules`, `kat`, `katal`, `kelvin`, `lb`, `liter`, `liters`, `lm`, `lumen`, `lux`, `lx`, `m`, `meter`, `meters`, `mile`, `miles`, `min`, `minute`, `minutes`, `mol`, `mole`, `mph`, `newton`, `ohm`, `ounce`, `ounces`, `oz`, `pascal`, `pound`, `pounds`, `rad`, `radian`, `radians`, `s`, `sec`, `second`, `seconds`, `siemens`, `sievert`, `tesla`, `ton`, `tonne`, `tonnes`, `tons`, `volt`, `w`, `watt`, `watts`, `weber`, `week`, `weeks`, `yard`, `yards`, `yd`, `°`, `Ω`.

- Explicit unit conversions with `->`
  ```
  60mph -> m/s
  500km/day -> km/h
  1mrad -> °
  52weeks -> days
  5in + 2ft -> cm
  atan(30cm / 2m) -> °
  6Mbit/s * 1.5h -> GB
  ```

- Variable assigments:
  ```
  r = 6000km
  vol = 4/3 * pi * r³
  density = 5g/cm³
  vol * density -> kg
  ```
  ```
  grav = 9.81m/s²
  len = 20cm
  2pi*sqrt(len/grav) -> ms
  ```
  Predefined constants: speed of light (`c`), Plancks constant (`hbar`), ...

  You can use `ans` (answer) to refer the the result of the last calculation.

- Commands:
  ```
  help, ?
  list, ls
  reset
  clear, cls
  quit, exit
  ```

Install
-------
In addition to the web interface, there is also a command line version which can by installed via [npm](https://www.npmjs.com/package/insect):
```sh
npm install -g insect
```

Build
-----
```sh
bower install
npm install
pulp -w browserify --skip-entry-point -m Insect --standalone Insect -O -t insect.js
```
