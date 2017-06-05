Dataset of Trump Flights Before He Became President
===

This repo includes data used in a June 1, 2017 story, [Everywhere Trump Traveled Before Air Force One](https://www.bloomberg.com/news/features/2017-06-01/this-is-where-trump-traveled-before-becoming-president).

The data was received via a Freedom of Information Act request to the Federal Aviation Administration for flights of three of his aircraft starting at the approximate date of their registrations through the day before Election Day, Nov. 7, 2016:

* Boeing 757-200 (N757AF), 2010-08-25 through 2016-11-07
* Cessna Citation X (N76DT), 2010-08-12 through 2017-10-02
* Sikorsky S-76 (N725DT), 2013-01-22 through 2016-11-07

## Files

The [data](data/) folder includes four files:

* [FOIA_2017-004225_Silver.xls](data/FOIA_2017-004225_Silver.xls) — The original spreadsheet provided to us in Excel format with one sheet for each aircraft: N757AF, N76DT, N725DT.
* [N757AF.csv](data/N757AF.csv), [N76DT.csv](data/N76DT.csv) and [N725DT.csv](data/N725DT.csv) — The Excel sheets broken out as CSV files.

## Caveats

### Airport codes

Most of the airports within the U.S. are listed using a three-letter IATA code. Airports outside of the U.S. list a four-letter ICAO code. For most U.S. airports, you can convert to ICAO by adding a `K` to the beginning of the code.

The following codes need a different modification:

* `KOA` should be `PHKO`
* `HNL` should be `PHNL`

The following codes need no modification:

* `26N`
* `JRA`

The code `EMI` is not listed in some databases but corresponds to a heliport in Westminster, MD at longitude `-76.9785719` and latitude `39.4950075`.

### Missing airport codes

Often, only one airport is listed for a helicopter flight. This happens when the destination or point of departure is not a standard airport.

### Completeness

The data represents information held by the FAA for these planes and might not capture all flights. From the story:

> One of the most striking things about these maps is what’s missing: no apparent flights to Russia. Given the multiple probes of his campaign’s links to Moscow, and deep curiosity about Trump’s business ties there, it’s an obvious thing to check. But there are none. Not even in November 2013, when Trump is known to have visited Moscow for the Miss Universe pageant. In fact, the data don’t show any foreign travel that month. So how’d he get there?

> There’s no indication of who is actually on the flights. And the FAA’s traffic records include only “flights that operated under instrument flight rules (IFR), or under visual flight rules (VFR) and were tracked by air traffic control in a radar environment.” One gap can be found in a 2012 Ireland-Turkey-Georgia-Scotland itinerary that appears to be missing its Turkey-to-Georgia leg.

### Possible errors

We removed flight `20100812391789`, the first flight in the helicopter's data, because it seemed to have been included in this data by error. The record indicates a different aircraft that may have been left over from an older registration.

We removed flight `20101016897001` from the helicopter's data because the listed flight from Maryland to Texas is outside that aircraft's range.

## Attribution

The provided data should be cited as `Federal Aviation Administration data obtained by Bloomberg News`.

If the data is used in an online story, the source line should include a link to this repository.
