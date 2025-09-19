
# Time units

So i gathered all these time units and i'll verify every one of them manually before adding them to my conversion library.

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
    
// Svedberg unit (sedimentation, not time but historically listed)
    1e-13                // svedberg (10^-13 seconds, used in biochemistry)
```
