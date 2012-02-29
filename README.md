Country Geolocation Data
========================

About
-----

Here are three PHP files I used when creating my [IP geolocator](http://usabilityetc.com/articles/serving-location-specific-content-with-ip-geolocation/). These files contain arrays that map two-letter [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country codes to the name of the country's continent and the name of the country's time zone.

### Country to Continent Mapping

The `CountryContinents.php` file contains two arrays. The `$CONTINENTS` array maps two-letter continent codes onto the name of the continent.

    $CONTINENTS = array(
        "AS" => "Asia",
        "AN" => "Antarctica",
        "AF" => "Africa",
        ...
    );

The `$COUNTRY_CONTINENTS` array maps two-letter country codes onto the two-letter  code of the country's continent.

    $COUNTRY_CONTINENTS = array(
        "AF" => "AS",
        "AX" => "EU",
        "AL" => "EU",
        ...
    );

### Country Latitude and Longitude

The `CountryLatLang.php` file contains the `$COUNTRY_LAT_LANG` array, which maps two-letter country codes onto the latitude and longitude of the centre of the country.

    $COUNTRY_LAT_LANG = array(
        "AD" => array(42.50, 1.50),
        "AE" => array(24.00, 54.00),
        "AF" => array(33.00, 65.00),
        ...
    );

### Country Time Zones

The `CountryTimeZones.php` file contains the `$COUNTRY_TIME_ZONES` array, which maps two-letter country codes onto the name of the country's time zone. Countries with multiple time-zones are represented by an array of time-zone name and time-zone longitude pairs. 

    $COUNTRY_TIME_ZONES = array(
        ...
        "AT" => "Europe/Vienna",
        "AU" => array(
                array("Australia/Adelaide", 138.583333),
                array("Australia/Brisbane", 153.033333),
                array("Australia/Broken_Hill", 141.45),
                ...
        ),
        "AW" => "America/Aruba",
        ...
    );

Data Accuracy
-------------

I found these files useful for my geolocator. As far as I know, the data is accurate but I make no guarantees of accuracy or completeness. Use at your own risk.
