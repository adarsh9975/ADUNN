# NMEA Sentences Used:

#### Courtesy:  Glenn Baddeley     http://aprs.gids.nl/nmea/#rmc

### $GPRMC

### Recommended minimum specific GPS/Transit data

eg1. $GPRMC,081836,A,3751.65,S,14507.36,E,000.0,360.0,130998,011.3,E*62

eg2. $GPRMC,225446,A,4916.45,N,12311.12,W,000.5,054.7,191194,020.3,E*68


           225446       Time of fix 22:54:46 UTC
           A            Navigation receiver warning A = OK, V = warning
           4916.45,N    Latitude 49 deg. 16.45 min North
           12311.12,W   Longitude 123 deg. 11.12 min West
           000.5        Speed over ground, Knots
           054.7        Course Made Good, True
           191194       Date of fix  19 November 1994
           020.3,E      Magnetic variation 20.3 deg East
           *68          mandatory checksum

### $GPGSA

### GPS DOP and active satellites

eg1. $GPGSA,A,3,,,,,,16,18,,22,24,,,3.6,2.1,2.2*3C

eg2. $GPGSA,A,3,19,28,14,18,27,22,31,39,,,,,1.7,1.0,1.3*35


            1    = Mode:
                   M=Manual, forced to operate in 2D or 3D
                   A=Automatic, 3D/2D
            2    = Mode:
                   1=Fix not available
                   2=2D
                   3=3D
            3-14 = IDs of SVs used in position fix (null for unused fields)
            15   = PDOP
            16   = HDOP
            17   = VDOP


### $GPVTG

### Track Made Good and Ground Speed.

eg1. $GPVTG,360.0,T,348.7,M,000.0,N,000.0,K*43

eg2. $GPVTG,054.7,T,034.4,M,005.5,N,010.2,K


           054.7,T      True track made good
           034.4,M      Magnetic track made good
           005.5,N      Ground speed, knots
           010.2,K      Ground speed, Kilometers per hour
           
           
# Parameters to be used

* Latitude
* Longitude
* Course made good
* Check Fix
* HDOP
* Track made good

# Tiny GPS Plus Functions to be used

#### Reference : http://arduiniana.org/libraries/tinygpsplus/

##### 'gps' is an object of tinygps library
* gps.location.lat() (double)
* gps.location.lng() (double)
* gps.speed.kmph() (double) (Optional)
* gps.course.deg() (double)
* gps.satellites.value() (int unsigned 32) (Optional) 
* gps.hdop.value()  (int 32)
* isValid() method will tell you whether the object contains any valid data and is safe to query.
* isUpdated() indicates whether the object’s value has been updated (not necessarily changed) since the last time you queried it.
* age() method returns the number of milliseconds since its last update. If this returns a value greater than 1500 or so, it may be a sign of a problem like a lost fix.
* charsProcessed() – the total number of characters received by the object
* sentencesWithFix() – the number of $GPRMC or $GPGGA sentences that had a fix
* failedChecksum() – the number of sentences of all types that failed the checksum test
* passedChecksum() – the number of sentences of all types that passed the checksum test
* You must continually feed the object serial NMEA data with encode().
* TinyGPSPlus.distanceBetween(start_lat,start_lng,end_lat,end_lng)
* TinyGPSPlus.courseTo(start_lat,start_lng,end_lat,end_lng)
* Human directions: TinyGPSPlus.cardinal(courseTo)

#### GPS Module used : NEO 6M (9600 baudrate)
