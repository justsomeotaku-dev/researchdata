
# Time units

So i gathered all these time units and i'll verify every one of them manually before adding them to my conversion library.

WHY ARE THERE SO MANY TIME UNITS AHHHHHHH and why am i making a converter for them...

ok i think length measurements are worse...

ok so https://en.wikipedia.org/wiki/Metric_prefix make si units a lot easier since u can just use the official si units and leave the rest aside.

```C
// Fundamental/Quantum time scales
    5.39e-44,            // Planck time
    1e-23,               // chronon (theoretical quantum time unit)
    
// SI prefixed units
    1e-24,               // yoctosecond
    1e-21,               // zeptosecond
    1e-18,               // attosecond
    1e-15,               // femtosecond
    1e-12,               // picosecond
    1e-9,                // nanosecond
    1e-8,                // shake (nuclear physics, 10 ns)
    1e-6,                // microsecond
    1e-3,                // millisecond
    1.0,                 // second
    1e3,                 // kilosecond
    1e6,                 // megasecond
    1e9,                 // gigasecond
    1e12,                // terasecond
    1e15,                // petasecond
    1e18,                // exasecond
    1e21,                // zettasecond
    1e24,                // yottasecond
    
// Computing time units
    1.0/60.0,            // jiffy (1/60 second, video frame)
    1.0/100.0,           // jiffy (1/100 second, computing)
    1.0/120.0,           // flick (1/705600000 second, but simplified here)
    
// Traditional time units
    60.0,                // minute
    90.0,                // moment (medieval: 1.5 minutes)
    900.0,               // point (medieval: 15 minutes)
    1800.0,              // ke (Chinese: 15 minutes)
    3600.0,              // hour
    
// Day-based units
    86400.0,             // day
    172800.0,            // Mars sol (24h 37m)
    604800.0,            // week
    1209600.0,           // fortnight
    
// Month variations
    2419200.0,           // lunar month (28 days)
    2551443.84,          // sidereal month
    2592000.0,           // month (30 days)
    2629746.0,           // month (average 30.44 days)
    2678400.0,           // month (31 days)
    
// Season and academic
    7889238.0,           // quarter (3 months)
    10519200.0,          // season (120 days)
    15778476.0,          // semester (6 months)
    15778476.0,          // half year
    
// Year variations
    31536000.0,          // common year (365 days)
    31557600.0,          // Julian year (365.25 days)
    31556925.2,          // tropical year (365.24219 days)
    31558149.5,          // Gregorian year (365.2425 days)
    31558432.0,          // sidereal year (365.25636 days)
    31622400.0,          // leap year (366 days)
    
// Historical multi-year periods
    63113904.0,          // biennium (2 years)
    94670856.0,          // triennium (3 years)
    126227808.0,         // quadrennium (4 years)
    126227808.0,         // olympiad (4 years)
    157784760.0,         // lustrum (5 years)
    315569520.0,         // decade (10 years)
    473354280.0,         // indiction (15 years)
    631139040.0,         // score (20 years)
    788923800.0,         // jubilee (25 years)
    946708560.0,         // generation (30 years)
    1577846760.0,        // half century (50 years)
    
// Long periods
    3155695200.0,        // century (100 years)
    31556952000.0,       // millennium (1000 years)
    
// Geological time scale divisions (Ma = million years)
    3.15569e13,          // megaannum/myr (million years)
    3.15569e16,          // gigaannum/gyr (billion years)
    3.15569e19,          // teraannum (trillion years)
    3.15569e22,          // petaannum
    3.15569e25,          // exaannum
    3.15569e28,          // zettaannum
    3.15569e31,          // yottaannum
    
// Astronomical time scales
    7.25e15,             // galactic year (230 million years)
    4.35e17,             // age of universe (13.8 billion years)
    3.15e18,             // cosmological decade (10^10 years)
    
// Extreme scales
    1.0e100,             // googol seconds
    3.15569e106,         // heat death timescale
    
// Hindu/Vedic time units (approximate)
    1.296e12,            // kalpa (day of Brahma, ~4.32 billion years)
    3.11e16,             // mahayuga (4.32 million years)

    Satya Yuga: 1,728,000 human years. 
    Treta Yuga: 1,296,000 human years. 
    Dvapara Yuga: 864,000 human years. 
    Kali Yuga: 432,000 human years. 

// Svedberg unit (sedimentation, not time but historically listed)
    1e-13                // svedberg (10^-13 seconds, used in biochemistry)
```
# Length units
```C
    // Planck scale and quantum measurements
    1.616255e-35,   // Planck length
    5.29177e-11,    // Bohr radius (first Bohr radius of hydrogen)
    2.8179e-15,     // classical electron radius
    1.32141e-15,    // Compton wavelength of electron
    2.10309e-16,    // Compton wavelength of proton
    8.768e-16,      // proton charge radius
    0.84184e-15,    // neutron charge radius
    
    // Subatomic particles and atomic scale
    1e-18,          // attometer
    1e-17,          // 10 attometers
    1e-16,          // 100 attometers
    1e-15,          // femtometer (fermi)
    1e-14,          // 10 femtometers
    1e-13,          // 100 femtometers
    1e-12,          // picometer
    1e-11,          // 10 picometers
    1e-10,          // angstrom
    1e-9,           // nanometer
    1e-8,           // 10 nanometers
    1e-7,           // 100 nanometers
    1e-6,           // micrometer (micron)
    1e-5,           // 10 micrometers
    1e-4,           // 100 micrometers
    1e-3,           // millimeter
    
    // Metric system - standard units
    1e-2,           // centimeter
    1e-1,           // decimeter
    1.0,            // meter (base unit)
    1e1,            // decameter (dekameter)
    1e2,            // hectometer
    1e3,            // kilometer
    1e4,            // myriameter
    1e5,            // 100 kilometers
    1e6,            // megameter
    1e7,            // 10 megameters
    1e8,            // 100 megameters
    1e9,            // gigameter
    1e12,           // terameter
    1e15,           // petameter
    1e18,           // exameter
    1e21,           // zettameter
    1e24,           // yottameter
    
    // Imperial/US customary units
    0.0000254,      // mil (thou)
    0.0254,         // inch
    0.3048,         // foot
    0.9144,         // yard
    1.8288,         // fathom
    5.0292,         // rod (pole/perch)
    20.1168,        // chain
    201.168,        // furlong
    1609.344,       // mile (statute mile)
    4828.032,       // league
    
    // Maritime and aviation units
    1852.0,         // nautical mile
    1853.184,       // nautical mile (UK)
    185.2,          // cable length (1/10 nautical mile)
    219.456,        // cable length (UK)
    
    // Historical and regional units
    0.4572,         // cubit (18 inches)
    0.508,          // cubit (20 inches)
    0.6096,         // cubit (24 inches)
    2.286,          // span (9 inches)
    0.1016,         // hand (4 inches)
    0.1143,         // palm (4.5 inches)
    0.0191,         // digit (0.75 inches)
    0.0254,         // barleycorn (1/3 inch)
    0.00423,        // line (1/12 inch)
    0.000353,       // point (1/72 inch)
    0.0003515,      // PostScript point
    0.0003527,      // TeX point
    0.000352778,    // DTP point
    
    // Surveying units
    0.201168,       // link
    4.04686,        // surveyor's chain (Gunter's chain)
    30.48,          // surveyor's rod
    
    // Textile and small measurements
    0.000127,       // denier (textile)
    0.0001,         // tex (textile)
    0.01,           // point (typography, 1/72.27 inch)
    0.000264583,    // pica (1/6 inch)
    
    // Atomic and molecular scales
    1.54e-10,       // carbon-carbon bond length
    3.4e-10,        // DNA base pair separation
    2.0e-10,        // typical atomic radius
    1.4e-10,        // hydrogen atom radius
    
    // Biological scales
    1e-6,           // typical cell diameter
    5e-6,           // red blood cell diameter
    1e-5,           // typical bacterium length
    1e-4,           // typical virus diameter
    0.1e-3,         // human hair diameter
    0.05e-3,        // spider silk diameter
    
    // Astronomical units
    6.96e8,         // solar radius
    1.496e11,       // astronomical unit (AU)
    4.243e16,       // light-year (precise)
    9.461e15,       // light-year (approximate)
    3.0857e16,      // parsec
    3.0857e19,      // kiloparsec
    3.0857e22,      // megaparsec
    3.0857e25,      // gigaparsec
    
    // Planetary and cosmic scales
    6.371e6,        // Earth radius (mean)
    1.737e6,        // lunar radius (mean)
    6.9551e7,       // Jupiter radius (equatorial)
    6.0268e7,       // Saturn radius (equatorial)
    2.5362e7,       // Neptune radius (equatorial)
    2.4622e7,       // Uranus radius (equatorial)
    6.0518e6,       // Venus radius (mean)
    3.3972e6,       // Mars radius (equatorial)
    2.4397e6,       // Mercury radius (mean)
    
    // Observable universe and large structures
    4.4e26,         // observable universe diameter
    3e25,           // typical galaxy cluster diameter
    1e21,           // typical galaxy diameter
    3e19,           // typical globular cluster diameter
    1e17,           // typical stellar nursery diameter
    1e16,           // Oort cloud diameter
    1e13,           // heliosphere diameter
    
    // Speed of light distances (time-based)
    2.998e8,        // light-second
    1.799e10,       // light-minute
    1.079e12,       // light-hour
    2.59e13,        // light-day
    7.77e15,        // light-month
    
    // Miscellaneous physical constants as lengths
    3.862e-13,      // reduced Compton wavelength of electron
    2.103e-16,      // reduced Compton wavelength of proton
    1.319e-15,      // reduced Compton wavelength of neutron
    
    // Additional imperial subdivisions
    0.000846667,    // point (1/72 inch, printing)
    0.00508,        // pica (1/6 inch, printing)
    0.001,          // point (metric, 1/2835 meter)
    
    // Asian traditional units
    0.303,          // shaku (Japanese foot)
    0.0303,         // sun (Japanese inch)
    0.3,            // chi (Chinese foot)
    0.033,          // cun (Chinese inch)
    1.8,            // ken (Japanese fathom)
    109.09,         // cho (Japanese)
    3927.27,        // ri (Japanese league)
    
    // Specialized scientific units
    1e-24,          // yoctometer
    1e-21,          // zeptometer
    1e21,           // zettameter
    1e24,           // yottameter
    
    // Nuclear and particle physics
    1e-15,          // fermi (femtometer)
    1.2e-15,        // nuclear radius unit
    10e-15,         // barn^(1/2) (cross-section unit)
    
    // String theory and theoretical physics
    1.616e-35,      // Planck length (theoretical minimum)
    
    // Computer/digital units
    0.000127,       // pixel (at 200 DPI)
    0.000254,       // pixel (at 100 DPI)
    0.0003528,      // pixel (at 72 DPI)
    
    // Wavelength references
    380e-9,         // violet light wavelength
    750e-9,         // red light wavelength
    21e-2,          // hydrogen line (21 cm)
    
    // Crystal lattice constants
    5.64e-10,       // silicon lattice constant
    4.05e-10,       // aluminum lattice constant
    3.57e-10,       // iron lattice constant
    2.87e-10        // tungsten lattice constant
```
Bit units
```C
    1,                           // bit
    8,                           // byte
    1024,                        // kilobit (Kb)
    8192,                        // kilobyte (KB)
    1048576,                     // megabit (Mb)
    8388608,                     // megabyte (MB)
    1073741824,                  // gigabit (Gb)
    8589934592,                  // gigabyte (GB)
    1099511627776,               // terabit (Tb)
    8796093022208,               // terabyte (TB)
    1125899906842624,            // petabit (Pb)
    9007199254740992,            // petabyte (PB)
    1152921504606846976,         // exabit (Eb)
    9223372036854775808ULL,      // exabyte (EB)
    1180591620717411303424ULL,   // zettabit (Zb)
    9444732965739290427392ULL,   // zettabyte (ZB)
    1208925819614629174706176ULL, // yottabit (Yb)
    9671406556917033397649408ULL, // yottabyte (YB)
    1237940039285380274899124224ULL, // ronnabit (Rb)
    9903520314283042199193193792ULL, // ronnabyte (RB)
    1267650600228229401496703205376ULL, // quettabit (Qb)
    10141204801825835211973625643008ULL  // quettabyte (QB)
```
