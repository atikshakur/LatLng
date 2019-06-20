# MyLoacation
Get Lat & Lng on andorid

#Usage

```
var driverLat: Double = 0.0
var driverLng: Double = 0.0

override fun onPermissionGranted() {
                val locationResult = object : MyLocation.LocationResult() {

                    override fun gotLocation(location: Location?) {

                        driverLat = location!!.latitude
                        driverLng = location.longitude

                        Toast.makeText(this@Registration, "$driverLat --SLocRes-- $driverLat", Toast.LENGTH_SHORT).show()
                    }

                }

                val myLocation = MyLocation()
                myLocation.getLocation(this@Registration, locationResult)
            }
```